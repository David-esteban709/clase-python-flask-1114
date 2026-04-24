# Clase Python Flask 1114

Este repositorio es una base MUY simple para empezar a trabajar con Flask.

La idea es que hoy quede listo el entorno y una app minima para que manana el curso pueda clonarlo y continuar desde aca sin arrancar de cero.

## Que es este repo

Es un proyecto inicial de Flask pensado para alumnos principiantes.

Incluye:

- una aplicacion minima en `app.py`
- una vista HTML simple en `templates/index.html`
- una consigna inicial en `tasks/tarea-1.md`
- comentarios breves y pedagogicos dentro del codigo

Importante: por ahora solo usamos lo minimo para levantar el servidor y ver algo en pantalla.
La ruta `/` aparece porque Flask necesita un punto de entrada para responder, pero la idea de rutas se vera con mas detalle manana.

## Requisitos

- Python 3 instalado
- Terminal abierta en la carpeta del proyecto

## Como crear el entorno virtual

Parate dentro de la carpeta del proyecto:

```bash
cd clase-python-flask-1114
```

Crear `.venv`:

```bash
python3 -m venv .venv
```

## Como activar `.venv`

En Linux o macOS:

```bash
source .venv/bin/activate
```

En Windows PowerShell:

```powershell
.venv\Scripts\Activate.ps1
```

Si el entorno esta activo, normalmente vas a ver `(.venv)` al principio de la linea de la terminal.

## Como instalar dependencias

Con el entorno virtual activado:

```bash
pip install -r requirements.txt
```

## Como ejecutar Flask

La forma mas simple para esta primera base es:

```bash
python app.py
```

Si todo sale bien, Flask va a mostrar una direccion local en la terminal, por ejemplo:

```text
http://127.0.0.1:5000
```

Abrila en el navegador.

## Que archivos mirar primero

1. `app.py`
2. `templates/index.html`
3. `tasks/tarea-1.md`

## Que hace cada parte

### `app.py`

Es el archivo principal.

- crea la aplicacion Flask
- define una respuesta minima para `/`
- arranca el servidor en modo de desarrollo

### `templates/index.html`

Es una pagina HTML muy simple.

- Flask la muestra cuando entramos a la app
- mas adelante servira para conectar Python con HTML usando plantillas

### `requirements.txt`

Lista las dependencias del proyecto.

- hoy solo necesitamos `Flask`

### `.gitignore`

Le dice a Git que archivos no conviene subir.

- por ejemplo `.venv`
- tambien archivos temporales de Python

### `tasks/tarea-1.md`

Trae una consigna corta y preguntas guia para practicar manana.

## Ideas utiles para manana

### Ejercicios cortos

1. Cambiar el titulo que aparece en el navegador.
2. Cambiar el mensaje principal de la pagina.
3. Agregar un segundo parrafo contando de que se trata la app.
4. Cambiar el texto del pie de pagina.
5. Probar que pasa si se guarda un cambio en HTML y se recarga el navegador.

### Preguntas guia para alumnos

1. Que archivo ejecutamos para levantar el servidor?
2. Para que sirve `.venv`?
3. Que guarda `requirements.txt`?
4. Que archivo contiene el HTML que vemos en pantalla?
5. Que parte del codigo arranca el servidor?
6. Que significa la ruta `/` en este ejemplo minimo?

## Objetivo de esta base

No entender todo hoy.

El objetivo de hoy es tener una estructura ordenada, poder levantar el proyecto y reconocer que archivo cumple cada funcion.
