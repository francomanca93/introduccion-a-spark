<div align="center">
    <h1>Introductorio de Spark</h1>
    <img src="https://imgur.com/FoB4GSE.png" width="">
</div>

## Tabla de contenido
- [Conociendo Apache Spark](#conociendo-apache-spark)
  - [Introducción a Apache Spark](#introducción-a-apache-spark)
    - [Spark VS Hadoop](#spark-vs-hadoop)
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


# Configuración

# Operaciones RDDs

# Data Frames y SQL

# Persistencia y particionado

# Conclusiones
