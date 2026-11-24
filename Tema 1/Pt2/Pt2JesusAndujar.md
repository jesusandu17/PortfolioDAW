# GitHub.md - Práctica de GitHub y Markdown

**Autor:** Jesús Andújar Fernández  
**Asignatura:** Despliegue de Aplicaciones Web

## 1. Introducción

GitHub es una página que sirve para guardar proyectos de programación y trabajar con otras personas. Utiliza Git, que permite guardar un historial de los cambios que hacemos en los archivos. Así podemos ver quién ha cambiado algo, recuperar versiones anteriores y organizar el trabajo. En este documento voy a explicar las funciones principales de GitHub con pasos fáciles.

## 2. Crear un repositorio

1. Entramos en https://github.com/ e iniciamos sesión.
2. Pulsamos `New repository` o el botón para crear un repositorio nuevo.
3. Escribimos el nombre y una descripción corta.
4. Elegimos si será público o privado.
5. Podemos marcar la opción de crear un `README.md` y pulsamos `Create repository`.

El repositorio es como una carpeta del proyecto en GitHub.

## 3. Crear carpetas y subir archivos

1. Entramos al repositorio y pulsamos `Add file` > `Upload files`.
2. Arrastramos los archivos y carpetas del proyecto. Si una carpeta está vacía, Git no la guarda por sí sola.
3. Escribimos un mensaje de cambio, por ejemplo `Subo la práctica 1`.
4. Pulsamos `Commit changes` para guardarlo.

Para crear un archivo sin subirlo, usamos `Add file` > `Create new file`. Si escribimos `tema1/README.md` como nombre, GitHub crea también la carpeta `tema1`.

## 4. Utilizar Markdown

Markdown permite dar formato al texto sin usar Word. El archivo suele tener extensión `.md`.

```md
# Título principal
## Apartado
Texto normal y **palabras importantes**.
- Primer punto
- Segundo punto
[Visitar GitHub](https://github.com/)
![Captura](imagenes/captura1.png)
```

El `README.md` se muestra directamente al abrir la carpeta del repositorio. Para que las imágenes se vean, hay que subirlas junto al Markdown y respetar las rutas.

## 5. Trabajar con Git desde la terminal

Primero entramos en la carpeta del proyecto y ejecutamos:

```bash
git init
git add .
git commit -m "Primera entrega"
```

Si el repositorio remoto ya existe, se puede enlazar con una URL real:

```bash
git branch -M main
git remote add origin URL_REAL_DEL_REPOSITORIO
git push -u origin main
```

La URL es un ejemplo pendiente de sustituir. No hay que pegar literalmente `URL_REAL_DEL_REPOSITORIO`.

Si ya tenemos un proyecto en GitHub, podemos descargarlo con:

```bash
git clone URL_REAL_DEL_REPOSITORIO
```

## 6. Guardar cambios y consultar el historial

Con `git status` vemos qué archivos han cambiado. Con `git add .` preparamos los cambios. Con `git commit -m "mensaje"` los guardamos en el historial local y con `git push` los subimos a GitHub.

```bash
git status
git add .
git commit -m "Actualizo el README"
git push
```

Para consultar las versiones guardadas podemos usar `git log --oneline`. Desde la página de GitHub también se puede pulsar `History` para revisar los cambios.

## 7. Crear ramas y pull requests

Una rama sirve para probar cambios sin tocar directamente la versión principal del proyecto. Por ejemplo:

```bash
git switch -c mejora-readme
```

Hacemos cambios y después:

```bash
git add .
git commit -m "Mejoro la documentación"
git push -u origin mejora-readme
```

En GitHub podemos abrir una `Pull request`, explicar lo que hemos cambiado y pedir que otra persona lo revise antes de unirlo a `main`.

## 8. Colaboradores, incidencias y seguridad

En la configuración del repositorio se puede invitar a colaboradores. También podemos abrir una `Issue` para dejar escrito un problema o una tarea pendiente.

Conviene añadir un `.gitignore` para no subir contraseñas, archivos temporales ni configuraciones privadas. En los trabajos en grupo es buena idea revisar las `Pull requests` antes de aceptar cambios.

**Nota:** no se han realizado cambios en un repositorio real desde este documento, así que no incluyo capturas inventadas. Si el profesor pide evidencias, hay que añadir capturas del repositorio personal.

## 9. Conclusión

Esta práctica me ha servido para entender que GitHub no es solamente una página para subir archivos. También permite llevar un control de todo lo que hemos hecho y trabajar con compañeros. Lo que más útil me parece es tener las prácticas organizadas por carpetas con su README, porque así el profesor puede entrar y ver el trabajo sin buscar entre muchos archivos.

## 10. Bibliografía

- https://docs.github.com/es
- https://docs.github.com/es/get-started
- https://www.markdownguide.org/basic-syntax/
