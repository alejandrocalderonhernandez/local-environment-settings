# 05_Redes_Sociales_y_Prompts_Visuales

## 1. Objetivo del Documento
Este archivo consolida las directrices para redactar el contenido promocional en redes sociales (Facebook, LinkedIn, X) y las reglas de ingeniería de prompts para generar la imagen acompañante en Gemini. El objetivo es entregar un paquete de marketing listo para copiar y pegar.

## 2. Reglas Estrictas de Publicación (El Algoritmo)
*   **Cero Enlaces en el Copy:** Para Facebook y LinkedIn, NUNCA incluyas URLs o códigos de cupones en el texto principal para evitar penalizaciones de alcance orgánico.
*   **Call To Action (CTA) Obligatorio:** En Facebook y LinkedIn, el cierre debe dirigir siempre al usuario al primer comentario: *"Revisa el primer comentario, ahí te dejé los enlaces con el descuento máximo."*

## 3. Especificaciones por Plataforma
*   **Facebook:** Tono conversacional, de ingeniero a ingeniero. Gancho emocional o pregunta inicial (ej. frustraciones de código). Párrafos cortos (máx. 2 líneas) y uso moderado de emojis.
*   **LinkedIn:** Tono profesional orientado al crecimiento de carrera (Tech Lead, entrevistas, arquitectura). Gancho de autoridad o dato de mercado. Incluir de 3 a 5 hashtags (Ej. #Java #SpringBoot #Backend).
*   **X (Twitter):** Límite estricto de **280 caracteres** (cuenta gratuita). Un solo mensaje directo y de alto impacto. Sin hilos. 

## 4. Guía de Estilo Visual para Gemini (Anti-Meme)
*   **Prohibiciones Visuales (Negative Prompting):** Prohibido pedir luces de neón, estética cibernética, código flotante, render 3D, aspecto plástico o Unreal Engine.
*   **Estilos Permitidos (Rotar en cada ejecución):**
    1.  *Candid Shot:* Fotografía 35mm, Kodak Portra 400, oficina real, desarrollador trabajando, monitor desenfocado en el fondo, luz natural.
    2.  *Flat Lay (Cenital):* Minimalismo técnico, vista desde arriba, escritorio limpio, teclado mecánico, libreta, café negro.
    3.  *Editorial Tech:* Fotografía macro, hardware/cables desenfocados, iluminación de estudio, alto contraste, estilo revista Wired.

## 5. Formato de Salida Exigido al Agente
Cuando ejecutes esta fase, tu única salida debe ser texto en Markdown estructurado exactamente en este orden:

### Publicación para Facebook
[Texto del post con el CTA al primer comentario]

### Publicación para LinkedIn
[Texto del post con el CTA al primer comentario y hashtags]

### Publicación para X (Twitter)
[Texto del post corto, máximo 280 caracteres]

### Prompt para Gemini
[Generar el prompt en **inglés** usando esta estructura exacta]:
`[Tipo de toma] of [Sujeto/Contexto], [Iluminación], [Cámara/Textura]. No neon lights, no floating code, no plastic skin, no 3D renders.`
