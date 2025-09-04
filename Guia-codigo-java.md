# Guía de estilo para código Java

Una guía de estilo es un conjunto de normas que aplicar a la hora de escribir código fuente en el lenguaje de programación al que van dirigidas. Su objetivo es crear estructuras de código fáciles de entender, no sólo para sí mismo sino también para cualquier programador, hacer más eficiente el proceso de desarrollo y conseguir que los programas sean más robustos y fáciles de mantener.

Durante la fase de codificación de un programa, el uso de una guía de código nos evitará tener problemas en:

1. **La calidad del programa**: Un programa mal escrito obliga a invertir mucho tiempo en descubrir qué es lo que está pasando y darle solución: Usar un estilo facilitará la lectura y la corrección rápida de errores.
2. **Mantenimiento del programa**: En las tareas de mantenimiento, la mayor parte del tiempo se pierde en leer y comprender el código existente, algo que parecía obvio en el momento de escribirse, pero que tiende a ser confuso cuando se vuelve a revisar, y aún más cuando el código lo escribió otra persona. Usar guías de código asegura que los programas sean más comprensibles.
3. **Comunicación entre programadores**: Dentro de un equipo de desarrollo es necesario utilizar un estilo común en el código que escriban, para mantener la homogeneidad y garantizar la comunicación entre sus miembros. **No estas desarrollando solo busca una solucion visionaria e integral**

Como cada programador tenemos nuestro propio estilo, es necesario establecer unos criterios comunes mínimos.

* [Mozilla](https://www.mozilla.org/es-ES/) tiene su *[
Coding style for developers](https://developer.mozilla.org/en-US/docs/Mozilla/Developer_guide/Coding_Style)*
* [GNU](http://www.gnu.org/) actualiza continuamente sus *[Coding standards](http://www.gnu.org/prep/standards/)*
* Hasta [Google](https://www.google.es/) tiene sus propias *[Google Style Guides](https://google.github.io/styleguide/javaguide.html)*



## El resumen del resumen

Lee el estilo de programacion que mejor se acomode a tus preferencias y en caso no lo quieras hacer...

>*Considera que en la primera entrega de código que hagas, **se descubrira que no lo hiciste**...*

### Formato de los ficheros
Sobre el formato de los ficheros que escribas:

1. Evita los **comentarios en línea (```//```)** en medio de los métodos, de las clases... *no es necesario que expliques en detalle tus ideas, prográmalas para que las entienda cualquiera*
2. **Líneas** de no más de **100 caracteres**, *para que podamos leer tu código los carcas que aún usamos el vi*.
3. Evita los **espacios al final de las líneas**, *se ven muy mal luego en git, afectan tu trabajo*
4. Procura **escribir bien**, sin faltas de ortografía, *no hablan bien de ti*
5. Usa **una línea en blanco** para separar bloques de código
6. Usa **espacios en blanco entre los operadores** lógicos en la condiciones, excepto en los operadores unarios


### Poniendo nombres
A la hora de poner nombre a las clases, métodos, variables... que escribas:

1. **NO uses abreviaturas** para nombrar nada
2. No pongas **el tipo en el nombre** *(```user_array, email_method CalculatorClass, ReportModule```)*
3. Para nombrar una clase **elige antes conceptos del dominio que indicar el patrón implementado** *( ```Guest vs NullUser, CachedRequest vs RequestDecorator```)*
4. Nombra los **miembros de una colección siempre en singular**
5. Procura que el nombre de la clase, variable o método **revele para qué sirve o qué hace**
6. Trata los **acrónimos** como palabras independientes *(```XmlHttpRequest``` y NO ```XMLHTTPRequest```)*

### Organización
Al escribir los métodos de las clases, trata de ser organizado, teniendo en cuenta:

1. Ordena los métodos de manera que **los que son llamados estén antes que los realizan las llamadas**
2. Ordena los métodos para que **el que es llamado y el que llama estén lo más cerca posible**.

### Y, en general,
1. Complejidad ciclomática: <8 a 12.
2. Paquetes : <20 clases.
3. Clases: <500 a 200 líneas, <20 métodos.
4. Métodos: <3 a 5 parámetros, <15 líneas.
5. Elimina redundancias, *(copy & paste)*.
6. Eliminar el código muerto, que nunca se ejecuta.
7. Haz un tratamiento de errores *(try - catch - finally)* y gestiona los Exceptions
8. Cobertura de test unitarios: >80%.


## Conoce tu IDE
Un Entorno de Desarrollo Integrado *(IDE en inglés)*, es  un  programa  diseñado  específicamente  para  facilitar  el  diseño  y  creación  de nuevo software. Para ello, integran distintas herramientas y funcionalidades en un único entorno, siendo la más importante el editor de código fuente, herramientas de construcción automáticas, un depurador y hasta de un completado inteligente de código, y todo para **optimizar y maximizar la productividad del programador en cada ciclo del desarrollo**.

[Eclipse](https://www.eclipse.org/downloads/) es uno de estos IDE, desarrollado originalmente por IBM que después liberó y ahora es mantenido por la [Eclipse Foundation](https://www.eclipse.org/membership/), una fundación independiente sin ánimo de lucro que fomenta la comunidad de código abierto. 

[IntelliJ IDEA](https://www.jetbrains.com/es-es/idea/) es un entorno de desarrollo multilenguaje que puede emplearse para la programación en Java y Kotlin para el desarrollo de aplicaciones de escritorio, web, distribuidas y para dispositivos móviles (Android). Tiene su version community.

Para el desarrollo de aplicaciones Java es recomendable buscar la version para desarrolladores, ya que incluirá todos los plugins que necesitará *(maven, git, sonarlint, etc)*

Averigua y aprende a usar atajos con los shortcuts

[Shortcuts Eclipse](https://www.digitalocean.com/community/tutorials/eclipse-shortcuts)

[Shortcuts Intellij](https://www.jetbrains.com/help/idea/mastering-keyboard-shortcuts.html)

### Configura tu IDE

Instalate los plugin que necesites para mejorar tu codificacion:

Asegúrate de que tienes **instalado [el plugin SonarLint](https://www.sonarlint.org/eclipse/)** y si no, [en este post](https://www.adictosaltrabajo.com/2014/10/08/eclipse-sonar-qube/) explican cómo poder hacerlo.
