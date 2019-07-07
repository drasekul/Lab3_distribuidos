# Lab3_distribuidos

## Integrantes:
 - Mario Caceres
 - Dragomir Sekul
 
# Análisis y Diseño de la Arquitectura Propuesta
 A continuación se presentará un diagrama del sistema distribuído que se quiso realizar.
 
 ![image alt](https://i.imgur.com/ay2EKSr.png)

Como se puede ver en la imagen las solicitudes hechas desde el frontend serán dirigidas a un proxy que llevará la consulta a uno de los brokers, esto será a partir del cual esta libre o el que tenga menos carga. Luego el broker selecionado enviará la consulta a uno de los servidores disponibles del sistema, el método de selecion del servidor puede ser tanto con un algoritmo Round Robin o con un similar al utilizado por los brokers. Finalmente el servidor realizará la consulta a la base de datos, que está replicada en cada uno de los servidores, y los resultados serán entregados al servidor y realizar el camino inverso para entregar los resultados de la búsqueda solicitada.


# Análisis del Rendimiento de la Arquitectura
