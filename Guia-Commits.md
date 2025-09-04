# Cómo deben ser los commits
Un *commit* es la actividad de guardar o subir los archivos que has modificado al repositorio en la rama en la que estás trabajando. **Las buenas prácticas invitan a hacer commit temprano y seguido**, siempre que:

1. El código no esté roto (que siempre compile)
2. Que el código no rompa las pruebas unitarias
3. Que no interfiera con el código de otro compañero

Esto permite volver a varios estados previos en caso de un bug difícil de rastrear. 

* Si confías en que puedes entregar los cambios correspondientes a toda la especificación sin problemas ya que la tarea no es muy compleja, entonces bastará con un solo commit.
* Si la tarea es demasiado compleja, divide la tarea en varias subtareas de modo que puedas asociar cada paso particular de la construcción a un commit específico.
* Si la tarea es simple, pero sin embargo consideras que te conviene más realizar varios commits por el motivo que sea, por ejemplo porque quieres entender mejor los cambios o te parece más ordenado, entonces hazlo de esa manera, no hay ningún problema. Si más tarde consideras que has hecho muchos commits para para algo muy simple, júntalos en uno solo.

Lo más importante es que **cada commit debe contener cambios funcionalmente completos** sin que rompan el código, los test unitarios ni generen conflictos.

Como ya sabrás, un commit están formado por los siguientes elementos:
* Ficheros que se han creado, modificado, renombrado o eliminado
* Un título de comentario 
* Un cuerpo del comentario
