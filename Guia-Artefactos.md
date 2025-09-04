# Repositorio de artefactos

Un repositorio de artefactos es un **espacio de almacenamiento desde el que poder recuperar e instalar paquetes de software en un ordenador**.
Este espacio se estructura en **directorios que incluyen una única versión numerada** para cada paquete, fruto de la **ejecución de la tarea de despliegue** del proceso de construcción automatizada *(build)*. 

Este espacio permite almacenar además, 
aquellos **componentes de terceros *(dependencias y librerías)*
que se necesitan para construir nuestras aplicaciones**,
y, del mismo modo, **generar nuestras propias
librerías** y compartirlas desde varias aplicaciones, fomentando así la compartición de código y centralizando su implementación. 

Además, al almacenar diferentes versiones de un mismo componente, permite **volver a usar una versión anterior** en caso de que sea necesario.


Disponer de estos repositorios es **fundamental cuando 
[se trabaja con Maven](Guia-Maven.md)**.
En el fichero ```pom.xml``` del proyecto, en la sección de ```<dependencies>```, se indican las librerías que usa nuestro proyecto y que *Maven* tratará de usar al compilar el proyecto. Para ello,

* lo primero que hace *Maven* es buscar estas dependencias en el **repositorio local** (por defecto en el directorio ```~/.m2/repository/```).
* si no las encontrara, entonces las buscará en el **repositorio público [Maven Central](https://mvnrepository.com/repos/central)** en Internet, las descargará e instalará en el repositorio local.
* La siguiente vez que *Maven* compile el proyecto, repetirá el mismo proceso, pero será más rápido porque no tendrá que descargar nada.
* En caso de que no pudiera encontrar alguna dependencia, *Maven* cancelará el proceso de construcción y no se generará ningún paquete binario distribuible.

Además de estos dos repositorios (local y público) por defecto, *Maven* ofrece la posibilidad de **configurar la búsqueda de dependencias en otros repositorios**:
* en el fichero de configuración  ```$M2_HOME/conf/settings.xml```
* en el propio ```pom.xml``` del proyecto mediante el tag ```<distributionManagement>```


## Repositorios privados
Usar únicamente los repositorios por defecto de *Maven*, presenta una serie de inconvenientes para las organizaciones:

1. Por un lado, **a la hora de utilizar librerías y componentes propios**: ¿Las suben a *Maven Central* y permiten que todo el mundo las use y las vea? ¿Las cuelgan en un sitio para que cada desarrollador las instale en local?
2. Por otro lado, **no se tiene ningún control sobre el contenido de estos repositorios *(local y público)***: Si en Maven Central eliminan una librería, ¿nuestras aplicaciones dejarán de compilar? ¿y si una librería incluye un virus? ¿cómo asegurarse de que el programador ha instalado la versión correcta en su equipo?


Para superar estos inconvenientes, las organizaciones cuentan con el **uso de repositorios privados en su propia red local**, aplicaciones que implementan un gestor de repositorios de artefactos y permiten controlar las librerías que almacenan sin depender de factores externos,  encontramos:

* [Artifactory](https://jfrog.com/open-source/)

 Acuerdense de que estos repositorios, permiten además:
 * **Cachear** el contenido de repositorios públicos y minimizar el consumo de ancho de banda
 * **Gestionar su contenido**, para evitar que los proyectos dejen de compilarse porque determinadas librerías no se encuentren en los repositorio públicos
 * Realizar automáticamente un **inventario de aquellas librerías inseguras**
 * Mantener un registro automático del **tipo de licencias de las librerías de terceros** que usan nuestras aplicaciones
 * Aplicar **políticas para la gestión del espacio** de almacenamiento





