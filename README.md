##Repositorio para probar codigo 
## y probar las ramas del árbol

## Comandos iniciales de git mediante CMD

>**git init:** se encarga de inicializar un archivo con la configuracion inicial del repositorio, todo repositorio necesita este archivo.
>**git add:** añade los archivos locales al git init y crea los identificadores unicos por archivos se puede usar de dos maneras principalmente *git add nombre_file* ó *git add .* el primero añade solo ese archivo en cuestion y el segundo añade todos los archivos modificados que se encuentren en ese directorio.
>**git commit -m "Mensaje de Referencia":** este es el mas importante motivo a que una vez se ejecuta se añaden todos los cambios que esten listos para ser subidos al repositorio con el comando a continuación.
>**git remote add origin URL-REPO-GIT:** al ejecutar este comando en la linea de comando añadimos al *git init* la direccion del repositorio en _github_. Cabe destacar que dicha direccion es publica y de acceso multiple.
>**git push -u origin master:** este comando se encarga de enviar los archivos al repositorio, ***solo*** aquellos que primero hayan sido añadidos con _git add_ y despues de haber hecho un _commit_. si la ejecucion fue en ese orden no deberia haber errores.

## Otra manera es solo añadir el repo y despues hacer un PUSH de los archivos 

#### Si esta es la opcion se debe ejecutar en la consola 
```
>git remote add origin URL_REPO_GIT
>git push -u origin master 
```

## Comando para crear branches desde la linea de comandos
##### Comenzemos con:

>**git branch** identifica las branches creadas en el repositorio por defecto todos vienen empaquetados con la ***master*** branch.
>**git branch nombre_rama** crea la branch en cuestion, donde se van a alojar ciertos cambios que no sean pertinentes para la ***master***. Una vez dentro se puede ejecutar ***git branch*** para confirmar que se esta dentro de la nueva rama del árbol.
>**git checkout nombre_rama** este selecciona y activa la nueva rama.
>**git checkout -b nombre_rama** es el mismo de arriba solo que crea la rama y la activa.
>**git branch -d nombre_rama** este comando elimina una rama identificada por el nombre.

>Al momento de unir el codigo se debe prestar atencion a la manera en la cual se ejecutan los comandos, el orden en el cual se insertan afecta la ejecucion por ende puede haber errores.

>Para unir el codigo de las dos ramas se debe ejecurtar un ***git pull*** antes si dicha rama esta desactualizada la misma hara un ***git merge*** por defecto y actualizara el codigo de una rama en la otra, y para subir los cambios se debe hacer un ***git push*** en la rama que este registrada en github por defecto ***master***.

>Para activdar (poder ver en ***Github***) una rama en especifico se debe hacer lo siguiente:
```
> git checkout -b dummy
> git push --set-upstream origin dummy
```
