# Tarea 1 - Levantar una aplicacion Flask desde cero

## Objetivo tecnico

Poner en marcha el proyecto en tu entorno local, entender para que sirve cada pieza minima del setup y verificar que la aplicacion responde en el navegador.

En esta primera clase no alcanza con "hacerlo andar". Tenes que empezar a distinguir que problema resuelve cada paso: aislamiento del entorno, instalacion de dependencias, arranque del servidor y renderizado de una plantilla HTML.

## Requisitos previos

- Tener Python 3 instalado y accesible desde terminal.
- Estar parado en la carpeta raiz del proyecto.
- Tener una terminal disponible para ejecutar comandos.
- Tener un navegador para comprobar la respuesta del servidor.

## Pasos para ejecutar el proyecto

1. Crear el entorno virtual:

   ```bash
   python -m venv .venv
   ```

   Este comando crea un entorno virtual dentro de la carpeta `.venv`. No es decoracion. Sirve para aislar las dependencias del proyecto y evitar mezclar paquetes de esta app con otros proyectos o con tu instalacion global de Python.

2. Activar el entorno virtual:

   ```bash
   source .venv/bin/activate
   ```

   Al activarlo, la terminal empieza a usar el interprete y `pip` de ese entorno. Si no entendes esto desde el arranque, despues instalas cosas "porque si" y no sabes donde quedaron.

3. Instalar las dependencias del proyecto:

   ```bash
   pip install -r requirements.txt
   ```

   `pip` instala los paquetes listados en `requirements.txt`. En este proyecto la dependencia principal es `Flask`, que es el framework que levanta el servidor web y conecta rutas con respuestas.

4. Ejecutar la aplicacion:

   ```bash
   python app.py
   ```

   Este comando corre el archivo principal del proyecto. Ahi se crea la aplicacion Flask, se define la ruta `/` y se inicia el servidor de desarrollo con `debug=True`.

5. Abrir la aplicacion en el navegador:

   Ingresa a la direccion local que aparece en terminal, normalmente `http://127.0.0.1:5000`.

   Si la pagina carga, significa que tu servidor esta escuchando solicitudes HTTP en tu maquina y que Flask encontro correctamente la plantilla HTML que debe renderizar.

6. Modificar la vista base y verificar el cambio:

   Edita `templates/index.html`, cambia al menos el `<title>` y el `<h1>`, guarda y recarga la pagina.

   Este paso existe para que veas la relacion concreta entre archivo fuente, servidor y resultado en navegador. Codigo que no observas, no lo entendes.

## Que hace cada parte base del proyecto

- `app.py`: punto de entrada. Crea la aplicacion, registra la ruta principal y arranca el servidor.
- `app = Flask(__name__)`: instancia la aplicacion Flask. Todavia no hace falta dominar todos sus argumentos, pero si entender que este objeto centraliza configuracion, rutas y ejecucion.
- `@app.route("/")`: define que funcion debe ejecutarse cuando alguien entra a la ruta raiz del sitio.
- `render_template("index.html")`: le dice a Flask que busque ese archivo dentro de `templates/` y lo entregue como respuesta.
- `templates/`: carpeta reservada por convencion para las plantillas HTML.
- `requirements.txt`: lista de dependencias necesarias para reproducir el entorno del proyecto.

## Preguntas de reflexion tecnica

1. Que problema concreto resuelve el entorno virtual en un proyecto Python?
2. Que diferencia hay entre instalar `Flask` globalmente y hacerlo dentro de `.venv`?
3. Por que `requirements.txt` forma parte del proyecto y no de tu maquina personal?
4. Cuando ejecutas `python app.py`, que archivo actua como punto de entrada y por que?
5. Que relacion hay entre la ruta `/`, la funcion `inicio()` y el archivo `templates/index.html`?
6. Que evidencia te da la terminal de que el servidor arranco correctamente?
7. Si cambias el HTML y el navegador muestra otra cosa, que te demuestra eso sobre el flujo entre backend y frontend en este proyecto?

## Entregable

La tarea se considera completa si puedes demostrar estas cuatro cosas:

1. El entorno virtual esta creado y activado.
2. Las dependencias se instalaron desde `requirements.txt`.
3. La aplicacion corre en tu maquina y responde en el navegador.
4. Modificaste `templates/index.html` y podes señalar exactamente donde se refleja ese cambio.

## Cierre

No estas aprendiendo a tipear comandos. Estas empezando a construir criterio tecnico. Si hoy entendes que levanta el servidor, de donde salen las dependencias y por que Flask encuentra esa plantilla, entonces arrancaste bien. Simple no significa superficial.
