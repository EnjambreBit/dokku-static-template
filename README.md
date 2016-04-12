# dokku-static-template

Un sitio demostración para subir a dokku.


## ¿Cómo hacer el deploy?

Primero tenes que vincular este repositorio dokku, seleccionando
el nombre del subdominio, por ejemplo "static-demo":

    git remote add dokku dokku@enjambrelab.com.ar:static-demo

Luego, una vez que se vinculó, realizá un push adicional a ese
repositorio remoto llamado dokku:

    git push dokku master

## ¿Cómo funciona?

Dokku utiliza scripts post-push que detectan e inicializan contenedores
docker para alojar la aplicación.

En este caso, el repositorio tiene dos archivos ``.static`` y ``.env``
que dokku utiliza para detectar que se trata de un sitio estático.
