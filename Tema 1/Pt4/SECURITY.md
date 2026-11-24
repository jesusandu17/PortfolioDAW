# SECURITY.md - Seguridad y accesibilidad del repositorio

Autor: Jesús Andújar Fernández

## 1. Objetivo

En esta práctica queremos que el proyecto del repositorio esté protegido y que cada compañero tenga acceso solo a lo que necesita. No deberíamos subir contraseñas ni archivos privados a Internet.

**Este documento contiene la configuración propuesta.** No tengo acceso al repositorio ni he podido invitar a compañeros desde aquí, por lo que las pruebas reales de permisos y sus capturas quedan pendientes.

## 2. Archivos que no se deben subir

He preparado un archivo `.gitignore` de ejemplo para un proyecto web. Ignora archivos `.env`, claves privadas, carpetas de dependencias, cachés, logs y configuraciones locales. Esos archivos pueden tener contraseñas, ocupar mucho o ser distintos en cada equipo.

Es importante recordar que `.gitignore` **no borra archivos ya subidos a Git**. Si alguno ya estaba registrado, hay que dejar de seguirlo y cambiar cualquier contraseña filtrada.

Comandos para comprobar las exclusiones:

```bash
git status
git check-ignore -v .env
```

Si un archivo privado ya estaba seguido por Git, se puede dejar de seguir (sin borrarlo del ordenador) con:

```bash
git rm --cached .env
git commit -m "Dejo de seguir el archivo privado"
```

Si ese archivo tenía claves reales, deben cambiarse; quitarlo del último commit no elimina automáticamente las claves de todo el historial.

## 3. Añadir un colaborador

1. Abrimos el repositorio en GitHub.
2. Entramos en `Settings` y buscamos `Collaborators` o `Access`.
3. Invitamos al compañero con su usuario de GitHub.
4. El compañero acepta la invitación.
5. Comprobamos si puede ver el proyecto y, con su permiso, hacer una prueba de edición en una rama.

## 4. Qué permisos necesita cada persona

| Rol | Qué puede hacer | Para quién lo utilizaría |
|---|---|---|
| Lectura | Ver y descargar los archivos | Profesor o persona que solo revisa |
| Escritura | Subir código y proponer cambios | Compañero que programa conmigo |
| Administración | Cambiar ajustes, permisos y opciones delicadas | Responsable del repositorio |

**Ojo:** en los repositorios propiedad de una cuenta personal, GitHub distingue principalmente entre propietario y colaboradores (con lectura y escritura). Para asignar roles separados como `Read`, `Write` y `Admin` normalmente se utiliza un repositorio de una organización. No debemos afirmar que hemos probado esos tres roles si el repositorio personal no permite asignarlos así.

## 5. Prueba real de permisos (pendiente)

| Prueba | Resultado esperado | Resultado real |
|---|---|---|
| Invitación | El compañero acepta el acceso | Pendiente de comprobar en GitHub |
| Lectura | Puede consultar los archivos | Pendiente |
| Escritura | Puede subir cambios autorizados | Pendiente |
| Administración | Puede configurar accesos solo si tiene ese rol | Pendiente, requiere organización/rol adecuado |

**Capturas que habría que añadir:** pantalla de colaboradores invitados, prueba de lectura, una rama o Pull Request creada por el compañero, y configuración de roles en caso de utilizar organización. No se adjuntan imágenes porque no se han realizado estas acciones.

## 6. Buenas prácticas de seguridad

- No compartir contraseñas ni tokens en el código o en las capturas.
- Utilizar ramas y Pull Requests para trabajar con cambios grandes.
- Proteger la rama principal y pedir revisión antes de unir cambios, si las funciones de la cuenta o repositorio lo permiten.
- Activar la verificación en dos pasos de GitHub.
- Guardar copias del repositorio y revisar las actualizaciones.
- Dar a cada persona solamente los permisos necesarios.

## 7. Recuperación de archivos

Si borramos algo por error, podemos revisar el historial de Git y recuperar una versión anterior. También podemos volver a clonar un repositorio remoto sano o utilizar una copia de seguridad.

Comandos útiles:

```bash
git status
git log --oneline
git restore archivo.txt
```

El último comando descarta cambios locales sin guardar en ese archivo. Hay que usarlo con cuidado. Una copia de seguridad aparte del propio GitHub nos protege mejor si se pierde el repositorio remoto.

## 8. Conclusión

Esta práctica me ha servido para entender que subir un proyecto a GitHub no consiste solamente en arrastrar archivos. También hay que revisar lo que compartimos y elegir bien quién puede modificar el código. Lo más importante es no publicar contraseñas, guardar el historial y revisar los cambios de los compañeros antes de aceptarlos.

## 9. Bibliografía

- https://docs.github.com/en/repositories/managing-your-repositorys-settings-and-features/repository-access-and-collaboration/permission-levels-for-a-personal-account-repository
- https://docs.github.com/en/organizations/managing-user-access-to-your-organizations-repositories/managing-repository-roles/repository-roles-for-an-organization
- https://docs.github.com/en/repositories/configuring-branches-and-merges-in-your-repository/managing-protected-branches
- https://git-scm.com/docs/gitignore
