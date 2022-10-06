# Tarea: Modelo dimensional y Base de datos

# Introducción

**Objetivo**

Comprender la relación entre un modelo dimensional y su representación en un modelo relacional, lo que se denomina modelo ROLAP. Adicionalmente, fortalecer la competencia de modelar multidimensionalmente a partir de un caso dado.

**¿Para qué?**

Practicar lo aprendido en el tutorial de modelado de datos y SQL y retomar el lenguaje SQL a nivel de creación de objetivos (DDL - _Data Definition Language_ y DML- _Data Manipulation Language_).

**¿Qué necesita?**

1. MySQL Workbench
2. Modelo multidimensional asociado al proceso de movimientos
3. Acceso al servidor de base de datos 
4. Script SQL [aqui](scriptTarea.sql)

# Enunciado
Ahora que sabe cómo crear modelos multidimensionales y hacer sentencias básicas con SQL, lo que debe hacer en la primera parte de esta tarea, es crear en una base de datos relacional las tablas que representan el modelo multidimensional compartido de Wide World Importers (WWI), poblarlas y consultarlas. En la segunda parte, va a practicar la competencia de modelar con un caso diferente al de la primera parte. A continuación encuentra el detalle de las actividades a realizar:  

1.	**MODELO ROLAP CASO MOVIMIENTOS WWImporters**: A partir del requerimiento analítico, modelo multidimensional y sentencias de creación de tablas que se dan como insumo para esta tarea, prepare los siguientes entregables. 
-	**Entregable CREATE**: Defina las sentencias para crear las tablas de **cliente** y **movimiento** de acuerdo con el modelo multidimensional que se comparte.
-	**Entregable INSERT**: Defina las sentencias para la inserción de 5 registros en todas las tablas del modelo multidimensional de **movimientos**.
-	**Entregable SELECT**: Defina las sentencias para consultar los datos de manera que le permita resolver el requerimiento analítico sobre **movimientos**. 
-	**Entregable EJECUTAR**: Ejecute las sentencias para crear, insertar y consultar la base de datos que refleje el modelo multidimensional dado y muestre los resultados obtenidos.

| **Tema analítico**                                               | **Análisis requeridos o inferidos**                                                                                                       | **Categoría del análisis (\*)** | **Procesos de negocio** | **Fuentes de datos**                                                    |
| ---------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------------------------------------------- | ------------------------------- | ----------------------- | ----------------------------------------------------------------------- |
| **Movimientos en el inventario de WWI** | Visualizar el número de productos que se movieron en el inventario en un rango de fechas por cliente, proveedor, y/o tipo de transacción | Consultas SQL             | Inventario                  | Movimientos, Tipos de transacción, Proveedores, Clientes y Productos  |

![Modelo moimientos](Img/Modelo%20movimiento.png)



2.	**MODELO MULTIDIMENSIONAL**: Proponga un modelo multidimensional para el siguiente caso, incluya detalles del modelo como el nivel de granularidad y aclaraciones que considere importantes, como parte de la entrega del mismo. Esta parte **NO** incluye la creación de tablas ni su población.

**ZOOALPES** 
Inspirado en el zoológico de Cali -- http://www.zoologicodecali.com.co 

ZooAlpes, más que un zoológico es un parque temático de carácter ambiental, con énfasis en fauna nativa, que ofrece una experiencia única de contacto con la riqueza natural y cultural, para el disfrute y la sensibilización del público de diversas edades e intereses.  
En la actualidad, los responsables de ZooAlpes, están interesados en diseñar estrategias para garantizar la calidad del servicio a sus visitantes, y al mismo tiempo garantizar el cuidado y protección adecuados de sus animales. Es por eso, que lo han contratado a usted para que les ayude a modelar el proceso de recorridos en el parque y de esta forma identificar si se están violando los derechos de los animales, lo que puede ir en detrimento del parque.  

Los análisis planteados pretenden identificar recorridos típicos de los visitantes: lugares que visita (atracciones – zorro cañero, danta amazónica, cusumbo solo, etc.-, juegos infantiles, restaurantes, áreas de descanso, baños, etc.), tiempo de estadía en cada uno de esos lugares, la franja horaria en la que están en los lugares, y si aplica, el valor adicional que pagaron, dependiendo del tipo de entrada que manejan.  

ZooAlpes maneja diferentes tipos de entrada entre los que se encuentran: plan **TRIBU** que permita el ingreso de 4 personas por 1 año (Todos los días 9:00 am a 4:30 pm) con un costo de $150.000, el plan **YACAIRA** que permite el ingreso ilimitado para 2 personas por 1 año (Todos los días 9:00 am a 4:30 pm) por $91.000, el plan **CAMINANTES**, que permite el ingreso ilimitado para 1 persona por 6 meses (Todos los días 7:00 am a 4:30 pm) por $91.000, o sin plan que no incluye pago por adelantado sino pago en el momento de ingresar al parque. Cada uno de estos tipos de entrada determina las atracciones que se pueden visitar sin costo adicional y las que requieren un valor adicional. Asociado a los planes, se tiene información del usuario que corresponde a su identificación, nombre, rango de edad, ocupación, estado civil, y número de hijos.   

### Herramientas de modelado online:
- LucidChart: https://www.lucidchart.com/pages/es
- GenMyModel: https://www.genmymodel.com/
