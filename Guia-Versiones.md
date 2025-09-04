# Números de versión

Cuando se trabaja en el desarrollo de una aplicación, constantemente se está modificando su código fuente para
añadir una nueva función *(feature)* o corregir un error *(bugfix)* en una característica. Este proceso incremental continuo
no está exento de errores y necesitamos un mecanismo que nos permita volver a un punto anterior sin errores y 
nos asegure la trazabilidad de la entrega de cambios.
Esto se consigue etiquetando con un número distinto cada cambio *(sea feature o bugfix)* acabado y
entregado al repositorio: Este número es lo que llamamos número de versión o simplemente versión de una aplicación.

La estructura de este número y el cuándo y cómo se incrementa es lo que se conoce como política de versionado de una aplicación.


## Política de versionado 

Para las aplicaciones Java desarrolladas


* **```X```**,**```Y```** y **```Z```**, son números enteros que responden a la expresión regular: ```[0-9]+```

* **```[Mayor]```** se corresponderá con los dos últimos dígitos del año en el que se publica la versión

* **```[Menor]```**, indicará el número de hito o milestone de la aplicación para ese año, que coincidirá con el número de versiones publicadas durante el año  `X`

* **```[Parche]```**, nos habla del número de rama, ya se de funcionalidad _(feature)_ o parche _(bugfix)_ que se ha aplicado e integrado sobre la versión `X.Y`.

Esta nomenclatura permite hacerse una idea,  simplemente viendo el número de versión, de:

1. **Cuánto de actualizado** está un proyecto: *Un número de versión que empiece por 12, ya nos está indicando que desde el año 2012 no hay nuevas versiones de ese artefacto*
2. **Cuán vivo está el desarrollo** observando el `Y`: *A mayor número, mayor número de hitos planificados para ese año, lo que se puede interpretar como un desarrollo más activo*
3. **La madurez del proyecto** observando el `Z`: *Cuánto mayor sea, será porque cada hito integra más bugfixes/features, señal de que el proyecto aún integra muchas ramas en cada hito*


