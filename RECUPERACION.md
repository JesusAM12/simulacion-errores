# Recuperación de archivos con Git

Simulé un error borrando accidentalmente el archivo `errores.sh` de mi repositorio.

1. Primero utilicé el comando `git reflog` para ver el historial de mis commits
y encontrar el commit donde el archivo aún existía. El hash de ese commit es `e3d7158`.
2. Luego, usé el comando `git checkout e3d7158 -- errores.sh` para recuperar
el archivo desde ese commit específico.
3. Finalmente, volví a agregar el archivo al área de staging y lo commité para reflejar la restauración.

Aprendí que si se elimina un archivo accidentalmente, Git tiene herramientas
como `git reflog` y `git checkout` que permiten recuperar fácilmente archivos perdidos
sin perder todo el trabajo.
