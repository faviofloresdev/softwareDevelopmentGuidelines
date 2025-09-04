# Control de PK de tablas
Una vez que hemos adoptado el modelo de [Integración continua](Guia-CI.md) y ajustado la [Entrega y despliegue de aplicaciones](Guia-CD.md) nuestra aplicación será desplegada en un contenedor. Los contenedores se consideran por naturaleza entidades "efimeras". Necesitamos una forma de procesar y almacenar para consulta el log de la aplicación. 

Usaremos [OpenSearch](https://opensearch.org/) para almacen y consulta logs 

## ¿Qué las tablas son las que se controla el PK?

Listado de las tablas que se deben considerar para asignación de PKs: 

- CAVAPPDB.ELEMENT_TABLES 

- CAVAPPDB.DEFINITION_TABLES 

- CAVAPPDB.REPORTS 

- CAVAPPDB.REPORT_FIELDS 

- CAVAPPDB.COMBOBOX_OPTIONS 

- CAVAPPDB.HTML_COMPONENTS 

- CAVAPPDB.MOVEMENT_TYPES 

- CAVAPPDB.CASH_MOVEMENT_TYPES 

- CAVAPPDB.BOND_LETTER_TYPE_MOVEMENTS 

- CAVAPPDB.CORRELATIVES (utiliza secuencia, pero para casos especiales donde se requiere manejarlo como constante lo que se está haciendo es incrementar el secuenciador para reservar el correlativo y así poder asignar) 

- CAVAPPALT.ALERT 

- CAVAPPALT.ALERT_TYPE_TEMPLATE 

- CAVAPPALT.SECURITY_ALERTS