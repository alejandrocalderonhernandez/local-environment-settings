# Udemy Curriculum Automation
**Versión:** 0.1 (Reverse Engineering)

> Este documento describe el flujo descubierto para automatizar la creación del currículo de un curso de Udemy utilizando exactamente los mismos endpoints que consume el frontend oficial.
>
> **Objetivo**
>
> Automatizar la creación de secciones (chapters), clases (lectures) y posteriormente la organización del currículo evitando la interfaz gráfica de Udemy.

---

# Estado actual

Actualmente se encuentra documentado:

- ✅ Crear Chapter
- ✅ Crear Lecture
- ✅ Crear Lecture con descripción
- ✅ Respuesta completa del endpoint de creación
- 🔄 Actualizar el currículo (pendiente de documentar completamente)
- 🔄 Subir Assets (Videos)
- 🔄 Asociar Asset a Lecture

---

# Flujo general

```text
Abrir Udemy

↓

Obtener Course ID

↓

Crear Chapters

↓

Crear Lectures

↓

Actualizar Curriculum

↓

Subir Videos

↓

Asociar Videos

↓

Publicar Curso
```

---

# Paso 1 - Obtener el Course ID

Antes de comenzar cualquier automatización es indispensable conocer el **ID del curso**.

Todos los endpoints utilizan este identificador.

Ejemplo

```text
https://www.udemy.com/instructor/course/4666014/manage/curriculum
```

En este ejemplo

```text
Course ID = 4666014
```

Este ID cambia para cada curso.

Nunca debe hardcodearse para reutilizar la librería.

Se recomienda almacenarlo como:

```javascript
const COURSE_ID = XXXXXXX;
```

---

# Arquitectura recomendada

Toda la automatización se ejecutará desde la consola del navegador.

No utilizar Postman.

No utilizar Node.

No utilizar Java.

La razón es que el código se ejecuta exactamente dentro del mismo contexto autenticado del frontend oficial de Udemy.

Por lo tanto:

- utiliza la misma sesión
- utiliza las mismas cookies
- utiliza el mismo contexto
- evita problemas de autenticación

---

# Crear una Sección (Chapter)

## Endpoint

```http
POST /api-2.0/users/me/taught-courses/{courseId}/chapters/
```

---

## Parámetros

| Nombre | Tipo |
|---------|------|
| courseId | Number |

---

## Headers

```http
Accept: application/json, text/plain, */*
Content-Type: application/json
X-Requested-With: XMLHttpRequest
Origin: https://www.udemy.com
Referer: https://www.udemy.com/instructor/course/{courseId}/manage/curriculum
```

Las cookies son enviadas automáticamente por el navegador.

No deben especificarse manualmente.

---

## Body

```json
{
    "title": "Introducción",
    "description": ""
}
```

---

## Respuesta esperada

Pendiente de documentar completamente.

Se espera una estructura similar a:

```json
{
    "id": 123456,
    "title": "Introducción",
    "description": "",
    "object_index": 1
}
```

---

# Crear una Lecture

## Endpoint

```http
POST /api-2.0/users/me/taught-courses/{courseId}/lectures/
```

---

## Headers

```http
Accept: application/json, text/plain, */*
Content-Type: application/json
X-Requested-With: XMLHttpRequest
Origin: https://www.udemy.com
Referer: https://www.udemy.com/instructor/course/{courseId}/manage/curriculum
```

---

## Body mínimo

```json
{
    "title": "Hola Mundo"
}
```

---

## Body recomendado

Actualmente se confirmó que también acepta descripción.

```json
{
    "title": "Hola Mundo",
    "description": "Clase introductoria."
}
```

---

# Respuesta (201 Created)

```json
{
    "_class": "lecture",
    "id": 57399245,
    "title": "Hola Mundo",
    "created": "2026-08-03T22:04:24.633097Z",
    "description": "Clase introductoria.",
    "title_cleaned": "hola-mundo",
    "is_published": false,
    "transcript": "",
    "is_downloadable": true,
    "is_free": false,
    "asset": null,
    "sort_order": 0,
    "labs": []
}
```

---

# Campos de respuesta

| Campo | Descripción |
|---------|------------|
| _class | Siempre "lecture". |
| id | Identificador de la lecture. |
| title | Nombre de la clase. |
| created | Fecha de creación. |
| description | Descripción enviada. |
| title_cleaned | Slug generado automáticamente por Udemy. |
| is_published | Siempre inicia en false. |
| transcript | Inicialmente vacío. |
| is_downloadable | true por defecto. |
| is_free | false por defecto. |
| asset | null. Posteriormente contendrá el video. |
| sort_order | Inicialmente 0. |
| labs | Lista vacía. |

---

# Observaciones

No es necesario enviar

- slug
- asset
- isPublished
- transcript
- labs

Udemy genera automáticamente:

- id
- created
- title_cleaned

---

# Modelo descubierto

Una Lecture es únicamente un contenedor.

```text
Lecture

├── id
├── title
├── description
├── asset
├── transcript
├── labs
└── metadata
```

El video todavía no existe.

Posteriormente se asociará mediante un Asset.

---

# Automatización basada en listas

El flujo recomendado consiste en construir primero una lista en memoria.

Ejemplo

```javascript
const chapters = [
    {
        title: "Introducción",
        lectures: [
            {
                title: "Bienvenida",
                description: ""
            },
            {
                title: "Instalación",
                description: ""
            }
        ]
    },
    {
        title: "Spring AI",
        lectures: [
            {
                title: "¿Qué es Spring AI?",
                description: ""
            },
            {
                title: "Primer Proyecto",
                description: ""
            }
        ]
    }
];
```

Posteriormente recorrer dicha lista.

```text
Crear Chapter

↓

Guardar Chapter ID

↓

Crear Lecture

↓

Guardar Lecture ID

↓

Crear Lecture

↓

Guardar Lecture ID

↓

Crear siguiente Chapter

↓

...
```

Todos los IDs deben almacenarse para el paso de actualización del currículo.

---

# Información importante

Cada creación devuelve un ID nuevo.

Ejemplo

```text
Lecture 1

↓

id = 57399245
```

Ese ID será utilizado posteriormente para construir el árbol del currículo.

Nunca asumir IDs consecutivos.

Siempre utilizar los IDs devueltos por la API.

---

# Actualización del currículo

Pendiente de documentar.

Actualmente se sabe que utiliza

```http
PUT /api-2.0/courses/{courseId}/instructor-curriculum-items/
```

y recibe un atributo llamado

```json
{
    "items": "..."
}
```

donde `items` es un **String** que contiene un arreglo JSON serializado.

Este endpoint será documentado una vez se termine de analizar completamente.

---

# Assets

Pendiente.

Actualmente todas las lectures son creadas con

```json
"asset": null
```

Falta descubrir:

- creación del asset
- subida del video
- asociación asset → lecture

---

# Pendientes

- Documentar completamente la creación de Chapters.
- Documentar la respuesta del endpoint de Chapters.
- Documentar GET del currículo.
- Documentar PUT del currículo.
- Documentar subida de videos.
- Documentar asociación de videos.
- Documentar publicación del curso.

---

# Notas de diseño

Toda la librería debe trabajar únicamente con los IDs obtenidos dinámicamente.

Nunca depender de:

- IDs hardcodeados.
- object_index.
- sort_order.
- title_cleaned.

Los únicos identificadores confiables son los IDs devueltos por la API.

---

# Buenas prácticas de ejecución

## Delays entre operaciones

Como medida de robustez, se recomienda introducir una pausa aleatoria entre operaciones consecutivas (creación de Chapters, Lectures y futuras operaciones sobre el currículo).

El objetivo es ejecutar las operaciones de forma secuencial y evitar ráfagas innecesarias de solicitudes.

Ejemplo:

```javascript
function sleep(ms) {
    return new Promise(resolve => setTimeout(resolve, ms));
}

function randomDelay(min = 1500, max = 3000) {
    return Math.floor(Math.random() * (max - min + 1)) + min;
}

await sleep(randomDelay());
```

Intervalo recomendado:

- Mínimo: **1500 ms**
- Máximo: **3000 ms**

Toda la automatización debe seguir el siguiente patrón:

```javascript
for (const lecture of lectures) {

    const createdLecture = await createLecture(lecture);

    console.log(`Lecture creada: ${createdLecture.id}`);

    await sleep(randomDelay());
}
```

**Importante:** evitar la ejecución concurrente (`Promise.all`) y esperar siempre a que cada petición finalice correctamente antes de iniciar la siguiente.
