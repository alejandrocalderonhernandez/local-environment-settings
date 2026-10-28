# cold-bytes-theme README

Paso 1: Instalar el generador de temas (vía npm)

Abre tu Terminal de macOS y ejecuta el siguiente comando:

npm install -g yo generator-code


Nota: Si te da un error de permisos (EACCES), ejecuta el comando agregando sudo al inicio (sudo npm install -g yo generator-code) e ingresa tu contraseña de Mac.

Paso 2: Generar la estructura del tema

1. En la terminal, entra a tu carpeta de proyectos (o donde quieras guardar el código fuente del tema):
   cd ~/Projects
   
2. Ejecuta el generador interactivo:
   yo code
   
3. Responde a las preguntas de la terminal con estos datos:
  ⚬ What type of extension do you want to create? \rightarrow Selecciona New Color Theme (usa las flechas del teclado y da Enter).
  ⚬ URL of an existing theme? \rightarrow Déjalo en blanco y presiona Enter.
  ⚬ What's the name of your extension? \rightarrow Nordic Mist Aurora
  ⚬ What's the identifier of your extension? \rightarrow nordic-mist-aurora
  ⚬ What's the description? \rightarrow Tema nórdico místico con acento turquesa, morado elegante y verde esmeralda.
  ⚬ Initialize a git repository? \rightarrow No (o Yes si usas Git).
  ⚬ Which base theme would you like to use? \rightarrow Selecciona Dark.

Paso 3: Pegar el JSON del tema

1. Entra a la carpeta recién creada:
   cd nordic-mist-aurora
   
2. Abre el archivo de configuración del tema que se generó dentro de la carpeta themes/:
   code themes/nordic-mist-aurora-color-theme.json
   
3. Reemplaza todo el contenido de ese archivo por el JSON del tema (el que incluye el morado elegante #B48EAD, verde esmeralda #00E676 y turquesa #00E5FF) y guarda el archivo (Cmd + S).

Paso 4: Instalarlo en local en tu VS Code

Para copiar tu tema directamente a la carpeta donde VS Code lee las extensiones locales en tu Mac, ejecuta:

cp -r ~/Projects/nordic-mist-aurora ~/.vscode/extensions/


Paso 5: Probar y Activar en VS Code

1. Abre tu VS Code.
2. Abre la paleta de comandos con Cmd + Shift + P.
3. Escribe Developer: Reload Window y presiona Enter (para que recargue las extensiones).
4. Presiona Cmd + K y luego Cmd + T (o abre Cmd + Shift + P y escribe Preferences: Color Theme).
5. Selecciona Nordic Mist Aurora de la lista.