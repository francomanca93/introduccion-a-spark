<div align="center">
    <h1>Introductorio de Spark</h1>
    <img src="https://imgur.com/FoB4GSE.png" width="">
</div>

## Tabla de contenido
- [Conociendo Apache Spark](#conociendo-apache-spark)
  - [Introducción a Apache Spark](#introducción-a-apache-spark)
    - [Spark VS Hadoop](#spark-vs-hadoop)
  - [Introducción a los RDDs y DataFrames](#introducción-a-los-rdds-y-dataframes)
    - [Características de los RDD](#características-de-los-rdd)
    - [Características de los DataFrame](#características-de-los-dataframe)
    - [¿Cuándo usar un RDD?](#cuándo-usar-un-rdd)
    - [¿Cuándo usar DataFrames?](#cuándo-usar-dataframes)
- [Configuración](#configuración)
- [Operaciones RDDs](#operaciones-rdds)
- [Data Frames y SQL](#data-frames-y-sql)
- [Persistencia y particionado](#persistencia-y-particionado)
- [Conclusiones](#conclusiones)

# Conociendo Apache Spark

## Introducción a Apache Spark

[Apache Spark](https://es.wikipedia.org/wiki/Apache_Spark) es un framework de trabajo para el desarrollo de grandes datos o big data y se preocupa de la velocidad y continuidad del procesamiento de datos, en contraparte de Hadoop que se preocupa por un almacenamiento grande de datos.

Podemos utilizar multiples lenguajes

- Java
- Scala (Spark corre nativamente aquí)
- Python
- R

> ¿Que nos es Apache Spark? No es una base de datos

![olap_OLTP](https://imgur.com/MiimHY1.png)

- **OLAP**: Es un sistema de recuperación de datos y análisis de datos en linea.

- **OLTP**: Es un sistema transaccional en línea y gestiona la modificación de la base de datos.

Spark debe estar conectado a un Data warehouse para poder aprovechar toda su funcionalidad.

![data_source_data_warehousing](https://imgur.com/LdvxsiA.png)

> [Historia de Apache Spark](https://es.wikipedia.org/wiki/Apache_Spark#Historia)

### Spark VS Hadoop

- Spark se enfoca en **procesamiento de datos desde la memoria ram**.

- Posee naturalmente un modulo para **ML**, **streaming** y **grafos**.

- No depende de un sistema de archivos.

![hadoop_vs_spark](https://imgur.com/ems5cAs.png)

## Introducción a los RDDs y DataFrames

### Características de los RDD

> At a high level, every Spark application consists of a driver program that runs the user’s main function and executes various parallel operations on a cluster. The main abstraction Spark provides is a [resilient distributed dataset (RDD)](https://spark.apache.org/docs/latest/rdd-programming-guide.html), which is a collection of elements partitioned across the nodes of the cluster that can be operated on in parallel. 

- **Principal abstracción de datos**: Es la unidad básica, existen desde su inicio hasta su versión 3.0.
- **Distribución**: Los RDD se dritribuyen y particionan a lo largo del clúster.
- **Creación simple**: Al no poseer estructura formalmente, adoptan las más intuitiva.
- **Inmutabilidad**: Posterior a su creación no se pueden modificar
- **Ejecución perezosa**: A menos que se realice una acción.

Las transformaciones no se ejecutan hasta que se llama a una acción. Por ejemplo: ordenar el RDD (**RDD.orderBy()**) no se ejecutara hasta que se mande una acción en este caso **RDD.orderBy().show()**.

| Transformaciones | Acciones |
| --- | --- |
| orderBy() | show() |
| groupBy()| take() |
| filter()| count() |
| select()| collect() |
| join() | save() |

![flujo_de_rdd](https://imgur.com/740Dm9u.png)

### Características de los DataFrame

- **Formato**: A diferencia de un RDD poseen columnas, lo cual les otorga tipos de datos.
- **Optimización**: Poseen una mejor implementación, lo cual los hace preferibles.
- **Facilidad de creación**: Se pueden crear desde una base de datos externa, archivo o RDD existente.

### ¿Cuándo usar un RDD?

- Cuando te interesa controlar el flujo de Spark.
- Si eres usuario Python, convertir a RDD un conjunto permite mejor control de datos.
- Estás conectándote a versiones antiguas de spark.

### ¿Cuándo usar DataFrames?

- Si poseemos semánticas de datos complicadas.
- Vamos a realizar tareas de alto nivel como filtros, mapeos, agregaciones, promedios o sumas.
- Si vamos a usar sentencias SQL.

# Configuración

# Operaciones RDDs

# Data Frames y SQL

# Persistencia y particionado

# Conclusiones
