### git log
Muestra todo el historial de commits

git log--pretty=format "%h -%an, %ar : %s"
Muestre el historial con el formato que indicamos.

### Limitar la salida del historial
git log -n : Cambiamos la n por cualquier número entero, por ejemplo git log -2, nos mostrará los 2 commits más recientes.

git log --after="2016-04-07 00:00:00": Muestra los commits realizados despues de la fecha especificada

git log --before="2016-04-08 00:00:00": Muestra los commits realizados antes de la fecha especificada

Las banderas del comando git log se pueden usar juntas según convenga, por ejemplo:
git log --after"2016-04-07 12:00:00" --before"2016-04-07 12:30:00"|

git log --decorate --oneline --graph -all
Este comando nos muestra el historial en una sola linea por commit.