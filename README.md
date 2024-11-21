Instrucciones para iniciar un proyecto con Vue.js
1. Descargar e instalar Vue.js
Descarga e instala Node.js si no lo has hecho aún.
Esto instalará automáticamente npm, el gestor de paquetes de Node.js.

Abre la terminal (CMD) y ejecuta el siguiente comando para iniciar un proyecto Vue:

npm create @latest
Este comando instalará y ejecutará create-vue, la herramienta oficial para generar proyectos Vue.js.

A continuación, se te presentarán varias preguntas para configurar tu proyecto. Puedes responderlas según tus necesidades o simplemente elegir las opciones predeterminadas presionando Enter:

✔ Nombre del proyecto: … <your-project-name>

✔ ¿Agregar TypeScript? … No / Sí

✔ ¿Agregar compatibilidad con JSX? … No / Sí

✔ ¿Agregar Vue Router para aplicaciones de una sola página? … No / Sí

✔ ¿Agregar Pinia para gestión de estados? … No / Sí

✔ ¿Agregar Vitest para pruebas unitarias? … No / Sí

✔ ¿Agregar una solución de pruebas de extremo a extremo? … No / Cypress / Nightwatch / Playwright

✔ ¿Agregar ESLint para la calidad del código? … No / Sí

✔ ¿Agregar Prettier para el formato del código? … No / Sí

✔ ¿Agregar la extensión Vue DevTools 7 para depuración? … No / Sí

Una vez que completes este paso, se creará el proyecto en una carpeta con el nombre que hayas especificado.

2. Instalar dependencias e iniciar el servidor de desarrollo
Navega a la carpeta de tu proyecto recién creado:

cd <your-project-name>
Instala las dependencias necesarias ejecutando:
npm install
Inicia el servidor de desarrollo:
npm run dev
Esto generará un enlace que se verá similar a:

VITE v4.0.0  ready in 300ms
Local:    http://localhost:5173/
Network:  http://192.168.1.1:5173/
Copia la URL del enlace, por ejemplo http://localhost:5173/, y pégala en tu navegador de preferencia.
¡Tu proyecto Vue.js ahora está en ejecución!
