# CourseFastApi

[![Code style: black](https://img.shields.io/badge/code%20style-black-000000.svg)](https://github.com/psf/black)
[![code style: prettier](https://img.shields.io/badge/code_style-prettier-ff69b4.svg?style=flat-square)](https://github.com/prettier/prettier)
[![js-standard-style](https://img.shields.io/badge/code%20style-standard-brightgreen.svg)](http://standardjs.com)

1.- Crear el entorno virtual de python

Tiene que ser exactamente con el nombre `.venv` para que no se creen confictos con el .gitignore

```ps
$ python -m venv .venv
```

2.- Activar el entorno virtual

```ps
# windows
$ .\.venv\Scripts\activate

# linux
$ source .\.venv\bin\activate
```

3.- Actualizar la libreria pip

```ps
$ python -m pip install --upgrade pip
```

4.- Intalar FastAPI

```ps
$ pip install fastapi uvicorn
```
<!--```ps
$ pip install -r .\requirements.txt
```

Nota: cada vez que se instale una nueva libreria en el proyecto es obligatorio ejecutar el siguiente comando para actualizar la lista de dependencias.

```ps
$ pip freeze > .\requirements.txt
``` -->
5.- Crear archivo de variables de entorno

En este archivo van las credenciales sencibles como el host y contraseña de la base de datos

```ps
$ copy .\.env.example .\.env
```

6.- Ejecutar el servidor

```ps
$ uvicorn main:app --reload
```

Nota: si necesita que el servidor sea accesible desde cualquier usuario dentro de la misma red, lo pueden hacer con el siguiente comando

```ps
$ uvicorn main:app --host 0.0.0.0 --port 8000 --reload
```