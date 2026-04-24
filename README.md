# Clase Python Flask 1114

## Que es este repo

Es un proyecto base de Flask.

Incluye:

- una aplicacion minima en `app.py`
- una vista HTML simple en `templates/index.html`
- una consigna inicial en `tasks/tarea-1.md`
- comentarios breves dentro del codigo

Incluye la configuracion minima para levantar el servidor y renderizar una vista inicial en la ruta `/`.

## Requisitos

- Python 3 instalado
- Terminal abierta en la carpeta del proyecto

## Como crear el entorno virtual

Ubicate dentro de la carpeta del proyecto:

```powershell
cd clase-python-flask-1114
```

Crear `.venv` en Windows:

```powershell
python -m venv .venv
```

Si usas Linux o macOS, el comando equivalente es:

```bash
python3 -m venv .venv
```

## Como activar `.venv`

En Windows PowerShell:

```powershell
.venv\Scripts\Activate.ps1
```

En Windows CMD:

```bat
.venv\Scripts\activate.bat
```

En Linux o macOS:

```bash
source .venv/bin/activate
```

Si el entorno esta activo, normalmente vas a ver `(.venv)` al principio de la linea de la terminal.

## Como instalar dependencias

Con el entorno virtual activado:

```powershell
pip install -r requirements.txt
```

## Como ejecutar Flask

Para ejecutar la aplicacion:

```powershell
python app.py
```

Si la aplicacion inicia correctamente, Flask va a mostrar una direccion local en la terminal, por ejemplo:

```text
http://127.0.0.1:5000
```

Abri esa direccion en el navegador.

## Que archivos mirar primero

1. `app.py`
2. `templates/index.html`
3. `tasks/tarea-1.md`

## Que hace cada parte

### `app.py`

Es el archivo principal.

- crea la aplicacion Flask
- define una ruta basica para `/`
- arranca el servidor en modo de desarrollo

### `templates/index.html`

Es la vista HTML inicial del proyecto.

- Flask la renderiza cuando se accede a la aplicacion
- sirve como base para trabajar con plantillas

### `requirements.txt`

Lista las dependencias del proyecto.

- actualmente solo incluye `Flask`

### `.gitignore`

Indica que archivos no se deben versionar.

- por ejemplo `.venv`
- tambien archivos temporales de Python

### `tasks/tarea-1.md`

Incluye una consigna inicial de trabajo.

## Objetivo

Contar con una base ordenada para instalar dependencias, ejecutar Flask y ubicar rapidamente los archivos principales del proyecto.

## Creditos

Design by profe Henry by kyrbot.com.
