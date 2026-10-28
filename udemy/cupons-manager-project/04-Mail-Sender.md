# 04_Mail_Sender

## 1. Objetivo y Reglas Estrictas (Cumplimiento Udemy)
Este documento instruye al agente sobre cómo redactar y enviar el correo con los cupones generados, cumpliendo estrictamente con los Términos de Servicio de Udemy para evitar la suspensión de la cuenta.

⚠️ **REGLAS CRÍTICAS DE UDEMY:**
*   **Canal Correcto:** Los cupones de descuento **JAMÁS** deben enviarse por la sección de "Anuncios Educativos" (Educational Announcements). Deben enviarse obligatoriamente por la sección **Correos Promocionales** (Promotional Emails).
*   **Frecuencia:** Udemy permite un máximo de **2 correos promocionales al mes** por curso. Antes de enviar, el agente debe verificar que cada curso seleccionado no haya alcanzado ese límite en el mes en curso.
*   **Enlaces Externos:** Está **PROHIBIDO** incluir enlaces a sitios fuera de Udemy (YouTube, sitios web personales, Patreon, etc.) en un correo promocional. Solo se permiten enlaces a cursos dentro de Udemy (las URLs de cupón generadas en el archivo `02`).

---

## 2. Cursos Aplicables (Audiencia del Correo)
El correo promocional se envía a los alumnos de **todos los cursos aplicables**, no solo a un curso emisor. Un curso es aplicable cuando cumple las tres condiciones:

1.  Está listado en `01_Courses_Inventory.md`.
2.  Tiene un cupón creado y validado por el usuario en la Fase 1 (archivo `02`).
3.  No ha alcanzado el límite de 2 correos promocionales en el mes en curso.

Si algún curso del inventario queda fuera por no cumplir alguna condición, el agente debe indicarlo al usuario junto con el motivo.

---

## 3. Instrucciones para la Redacción del Asunto (Subject Line)
Para maximizar la tasa de apertura y evitar los filtros de spam de Udemy, el asunto debe cumplir estas directrices comprobadas:
*   No usar mayúsculas sostenidas (ALL CAPS).
*   No usar signos de exclamación excesivos.
*   Evitar palabras desencadenantes de spam como: "Gratis", "Oferta", "Venta", o "% de descuento".
*   Utilizar un enfoque de urgencia sutil, curiosidad o el inicio del framework de copywriting seleccionado en el archivo `03`.

---

## 4. Estructura del Cuerpo del Correo Promocional
El agente construirá el mensaje combinando la estrategia del archivo `03` y los enlaces del archivo `02`, estructurado de la siguiente manera:

1.  **Apertura y Gancho:** Iniciar con el gancho definido en `03_Copywriting_Strategies_and_Angles.md` para captar el interés inmediatamente.
2.  **Desarrollo del Copy:** Aplicar el framework persuasivo (PAS, AIDA o BAB) proporcionando valor técnico sobre el desarrollo backend y Java, conectando el dolor del estudiante con la solución.
3.  **Lista de Cupones (El Catálogo):** Presentar los enlaces de cupón de todos los cursos aplicables con una estructura limpia.
    *   *Ejemplo de formato:*
        *   🚀 **[Título del Curso 1]** - Domina esta habilidad hoy: [URL del cupón 1]
        *   ⚙️ **[Título del Curso 2]** - Mejora tu arquitectura: [URL del cupón 2]
4.  **Cierre y Urgencia:** Recordar sutilmente que el acceso con este precio específico tiene una ventana de tiempo limitada.

---

## 5. Aprobación del Borrador
Antes de cualquier envío, el agente debe presentar al usuario:
*   El asunto.
*   El cuerpo completo del correo.
*   La lista de cursos aplicables que recibirán el correo (y los excluidos con su motivo).

El envío solo procede tras la aprobación explícita del usuario.

---

## 6. Ejecución de Envío (Browser Automation)
Una vez aprobado el borrador, el agente procederá con el envío:

1.  En la sesión activa de Udemy, entra al panel de instructor.
2.  Despliega **Comunicaciones** y selecciona **Correos Promocionales** (Promotional Emails).
3.  Haz clic en **Redactar** (Compose).
4.  En el selector de destinatarios, **selecciona todos los cursos aplicables** definidos en la sección 2.
    *   Si la interfaz no permite seleccionar varios cursos en un mismo correo, repite los pasos 3 a 8 para cada curso aplicable, usando el mismo asunto y cuerpo aprobados.
5.  Pega el asunto aprobado.
6.  Pega el cuerpo del correo aprobado.
7.  Verifica por última vez que no haya enlaces externos y que los cursos seleccionados coincidan con la lista aprobada.
8.  Haz clic en **Enviar** (Send).
9.  Notifica al usuario qué cursos recibieron el correo promocional (y cualquier envío que haya fallado) y avanza a la creación de los posts en redes sociales (Archivo `05`).