# 00_Workflow_Orchestrator

## 1. Objetivo del Orquestador
Este archivo es el cerebro central de la automatización para el proyecto `cupons-manager`. Dicta el orden exacto de ejecución de los archivos de conocimiento presentes en el contexto y establece una pausa obligatoria de aprobación humana para dividir el trabajo en dos fases estrictas.

---

## 2. PASO 1: Creación de Cupones (Ejecución de `01_Courses_Inventory.md` y `02_Udemy_Navigation_Protocol.md`)
Cuando el usuario inicie el proceso, el agente debe ejecutar exclusivamente esta fase consultando los archivos mencionados:

1.  **Lectura de Inventario:** Lee y carga en memoria los datos del archivo `01_Courses_Inventory.md`.
2.  **Navegación y Creación:** Ejecuta las instrucciones del archivo `02_Udemy_Navigation_Protocol.md` para navegar en Udemy y crear los cupones.
3.  **Salida Esperada:** Entrega al usuario una lista estructurada con los enlaces de los cupones recién creados.
4.  **🛑 PAUSA OBLIGATORIA:** Detén toda actividad. No generes textos, no envíes correos. Espera a que el usuario valide la lista de cupones y te dé la orden explícita de "continuar".

---

## 3. PASO 2: Marketing y Distribución (Ejecución de `03_Copywriting_Strategies_and_Angles.md`, `04-Mail-Sender.md` y `05_Redes_Sociales_y_Prompts_Visuales.md`)
Una vez que el usuario apruebe el Paso 1 y dé la orden de continuar, el agente procederá integrando los siguientes archivos:

1.  **Estrategia de Copywriting:** Lee el archivo `03_Copywriting_Strategies_and_Angles.md` para definir el framework, la temática de la campaña y redactar el texto persuasivo.
2.  **Envío de Correos Automático:** Ejecuta el archivo `04-Mail-Sender.md`. Usa los textos generados y los enlaces del Paso 1 para navegar en Udemy, redactar y enviar los correos promocionales de cada curso de forma autónoma.
3.  **Salida Esperada (Redes Sociales y Visuales):** Ejecuta el archivo `05_Redes_Sociales_y_Prompts_Visuales.md` y entrégale al usuario el documento Markdown final que contenga:
    *   El post para Facebook.
    *   El post para LinkedIn.
    *   El post para X (Twitter).
    *   El prompt en inglés para generar la imagen promocional en Gemini.

## 4. Fin del Flujo
El proceso termina exitosamente cuando los correos promocionales han sido enviados mediante la interfaz de Udemy y el usuario recibe el paquete final de textos listos para sus redes sociales.
