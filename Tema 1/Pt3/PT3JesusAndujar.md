# Actividad 1. Evaluación y uso de un generador de documentación

Autor: Jesús Andújar Fernández  
Asignatura: Despliegue de Aplicaciones Web

## 1. Introducción

En esta práctica voy a comparar varias herramientas para documentar código. La documentación sirve para que otra persona pueda entender para qué es cada función sin tener que investigar todo el programa. Después voy a probar una herramienta con un proyecto pequeño de ejemplo.

**Importante:** en el material entregado solo venía el enunciado, no el código del proyecto del curso pasado. Por eso la aplicación práctica que adjunto es una **demostración nueva en Python**. Para cumplir literalmente el ejercicio del profesor habría que sustituirla por un proyecto real del curso anterior y generar otra vez su documentación.

## 2. Comparación de herramientas

| Herramienta | Para qué se usa | Facilidad | Integración | Formatos habituales | Comunidad y dificultad |
|---|---|---|---|---|---|
| Javadoc | Documentar proyectos Java | Media | Muy buena con Java e IDE | HTML | Muy conocida; hay que aprender etiquetas como `@param` |
| JSDoc | Documentar JavaScript | Fácil-media | Funciona con Node.js y editores | HTML, y otros con complementos | Bastante utilizada; comentarios sencillos |
| Sphinx | Documentar Python y proyectos técnicos | Media | Python, docstrings y reStructuredText/MyST | HTML, PDF mediante extensiones/herramientas | Comunidad grande; cuesta configurarla al principio |
| Doxygen | Documentar varios lenguajes como C++ | Media | Se puede usar en muchos proyectos | HTML, LaTeX y PDF mediante LaTeX | Herramienta veterana; muchas opciones |
| MkDocs | Crear documentación a partir de Markdown | Fácil | Muy cómodo con Git y GitHub | HTML; PDF con plugins | Fácil de aprender, pero no analiza funciones por sí solo |
| Swagger / OpenAPI | Describir y probar APIs REST | Media | APIs de muchos lenguajes | HTML interactivo y formatos OpenAPI YAML/JSON | Muy usado en APIs; hay que definir los endpoints |

Estas herramientas no hacen exactamente lo mismo. Javadoc, JSDoc y Doxygen se centran más en el código. MkDocs sirve sobre todo para montar una web de documentación. Swagger/OpenAPI está pensado para las APIs.

## 3. Herramienta elegida

He elegido **pydoc**, que viene con Python y puede generar una página HTML usando los docstrings de los archivos. Es una forma fácil de empezar porque no tenemos que instalar programas extra. No estaba entre los ejemplos del enunciado, pero cumple la misma idea de generar documentación automáticamente a partir del código.

## 4. Aplicación práctica de ejemplo

He preparado un archivo llamado `gestor_tareas.py`. Contiene funciones para añadir, completar y listar tareas. Cada función tiene un docstring que explica qué hace, qué recibe y qué devuelve.

El archivo está en la carpeta `proyecto_ejemplo/` que acompaña a este documento. Para probarlo en Ubuntu:

```bash
cd proyecto_ejemplo
python3 gestor_tareas.py
```

Para generar la documentación automáticamente:

```bash
cd proyecto_ejemplo
python3 -m pydoc -w gestor_tareas
```

Al terminar aparece el archivo `gestor_tareas.html`, que también he incluido en la entrega. Se puede abrir en Firefox y ver la descripción del módulo y de sus funciones.

## 5. Resultado

La herramienta ha permitido obtener un HTML a partir de los comentarios del código de demostración. Así, cuando alguien abre el documento, puede saber qué hace cada función sin tener que revisar todo el programa.

**Lo que quedaría pendiente para aplicar el ejercicio a un proyecto verdadero del curso pasado:** copiar aquí el código original, comentar sus clases y funciones, ejecutar el generador de nuevo y guardar las capturas del resultado. No he inventado capturas ni afirmo haber aplicado la herramienta al proyecto antiguo.

## 6. Reflexión personal

La prueba me ha parecido bastante sencilla. Lo más largo ha sido escribir los comentarios de las funciones, pero luego crear la documentación fue rápido. Me gusta que, si cambio el código y actualizo los docstrings, puedo volver a generar el HTML sin escribir todo desde cero. La desventaja es que, si escribimos comentarios malos o no los actualizamos, la documentación también estará mal. Para un trabajo en grupo sí la recomendaría, porque ayuda a que todos entiendan el programa. En un proyecto más grande utilizaría Sphinx o MkDocs para tener también menús y páginas con explicaciones.

## 7. Bibliografía

- Documentación de `pydoc`: https://docs.python.org/3/library/pydoc.html
- Javadoc: https://docs.oracle.com/en/java/javase/21/javadoc/
- JSDoc: https://jsdoc.app/
- Sphinx: https://www.sphinx-doc.org/
- Doxygen: https://www.doxygen.nl/
- MkDocs: https://www.mkdocs.org/
- OpenAPI: https://swagger.io/specification/
