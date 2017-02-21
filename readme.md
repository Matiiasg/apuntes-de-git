#Zonas de GIT
1. Directorio de Trabajo
2. Área de preparación
3. Directorio GIT

##Flujo de trabajo básico en GIT
1. Modificas una serie de archivos en tu directorio de trabajo.
2. Preparas los archivos, añadiéndolos a tu área de preparación.
3. Confirmas los cambios, lo que toma los archivos tal y como están en el área de preparación y almacena esa copia instantánea de manera permanente en tu directorio de Git.

##Configurando GIT por primera vez
```
git config --global user.name "John Doe"
git config --global user.email johndoe@example.com
git config --global core.editor nano
git config --list
```
## Configurando SSH en Widnows

1. Creamos una carpeta llamada `llaves-shh` en el disco `C` para evitar problemas de rutas

2. Ejecutamos el comando `ssh-keygen -t rsa -C "mi-correo@ejemplo.com"`
El correo debe ser el mismo con el que nos registramos en Github para evitar posibles problemas.
Dejamos el passphrase vacío y damos enter.
Cuando nos pide la rita escribimos `/c/llaves-ssh/github_rsa`

3. Iniciamos shh-agent en backfround ejecutando el comando `eval "$(ssh-agent -s)"`

4. Agregamos la llave ssh generada a ssg-agent ejecutando el comando `ssh-add /c/llaves-ssh/github_rsa`

5. Usar el comando `cat /c/llaves-ssh/github_rsa.pub`
Con este comando vemos el contenido del archivo, copiamos todo el texto que nos muestra.

6. Ir a las configuraciones de nuestro perfil de Github y agragar un nueva llame SSH con el contenido que hemos copiado de `github_rsa.pub`

Desde ahora podemos hacer pull y push sin que Github nos esté pidiendo usuario y clave de acceso.

