# Que es SQL y No SQL

Tomado de:

https://www.youtube.com/watch?v=cLLKVd5CNLc&t=630s

## Que es una BD

- Coleccion organizada de informacion
- Controlada por un DBMS (data base management system)
- Modelada por filas y columnas
- Consultas faciles
- Faciles de actualizar, modificar, controlar, organizar
  
## SQL y NoSQL

- **SQL** lenguaje estructurado de consultas, 
  - son relacionales, 
  - las tablas son entidades, 
  - su esquema es predefinido definiendo tablas, columnas, llaves, relaciones etc. lo cual puede restringir 
  - todo se especifica del como se va a trabajar
  - son escalables verticalmente, si deseo aumentar capacidad entonces aumento cpu, ram 
  - Sintaxis estandarizada y definida por normas ANSI
  - Oracle, Mysql, Postgresql, Sqlite, Sql Server, MariaDB, 
  - Se aplican en proyectos donde se prioriza la consistencia / integridad sacrificando disponibilidad 
  - Usadas en Bancos (transacciones)

- **NoSQL** no usan la estructura SQL, 
  - no existe relacion entre las entidades,
  - el esquema es dinamico, se define a medida que se trabaja en los datos
  - usan documentos, por ejemplo los tipo JSON, XML, (claves: valor), grafos
  - son escalables horizontalmente, en este caso se fragmentan los datos que se traten en diferentes servidores
  - La sintaxis depende de cada base de datos, no hay estandar definido 
  - MongoDB, Redix, Neo4j (grafos), Apache Cassandra
  - Se aplican en proyectos en donde se prioriza la disponibilidad a costa de integridad
  - Usadas en Chats online, 