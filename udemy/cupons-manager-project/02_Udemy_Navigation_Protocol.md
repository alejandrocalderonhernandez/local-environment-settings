# 02_Udemy_Navigation_Protocol

## 1. Objetivo del Protocolo
Este documento establece las instrucciones operativas para que el agente de IA automatice la creación de cupones de máximo descuento de forma manual (curso por curso) a través de la interfaz visual de Udemy, y extraiga los enlaces generados. 

⚠️ **REGLA ESTRICTA:** En este paso NO se debe redactar, programar ni enviar ningún correo o anuncio. La tarea termina exclusivamente con la entrega de la lista de enlaces de cupones creados.

---

## 2. Fase de Ejecución: Creación Manual de Cupones (Curso por Curso)
**Instrucciones para el Agente (Browser Automation):**

Para cada curso listado en el archivo `01_Courses_Inventory.md`, realiza la siguiente secuencia de navegación en el navegador donde la sesión de Udemy ya está iniciada:

1.  Ve al panel de instructor y entra a la página de gestión del curso específico.
2.  En el menú lateral izquierdo, haz clic en **Promociones** (Promotions).
3.  Haz clic en el botón **Crear nuevo cupón** (Create new coupon).
4.  Selecciona el tipo de cupón: **Precio Personalizado** (Custom Price). Esto es obligatorio porque permite mantener el precio más bajo posible durante un periodo largo (31 días), a diferencia de otros que duran solo 5 días.
5.  Configura los parámetros del cupón:
    *   **Precio:** Selecciona o ingresa el precio más bajo permitido por la plataforma (ej. 139 MXN o el mínimo habilitado en el selector).
    *   **Código del cupón:** Escribe un código identificador (Ej. `MAXDESCUENTO_[MES][AÑO]`).
    *   **Fecha de inicio:** El día actual.
    *   **Duración:** 31 días (el máximo permitido para el precio personalizado).
6.  Haz clic en el botón para revisar y confirmar la creación del cupón.
7.  Una vez creado exitosamente, **copia la URL directa del cupón** que aparece en la lista de promociones activas.
8.  Repite los pasos del 1 al 7 para el siguiente curso en el inventario.

---

## 3. Salida Esperada (Checkpoint)
Una vez que hayas iterado por todos los cursos, **DETENTE**. No navegues a la pestaña de comunicaciones.

Tu única salida en esta fase debe ser una lista estructurada que contenga el título de cada curso y su respectivo enlace de descuento generado. 

**Formato de salida requerido:**
*   [Título del Curso 1]: [URL del cupón]
*   [Título del Curso 2]: [URL del cupón]
*   [Título del Curso 3]: [URL del cupón]

**Espera la aprobación del usuario antes de pasar a la fase de redacción y envío de correos.**
