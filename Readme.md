# En SQL null es null, vacio esta vacio

Tomado de:

https://www.aluracursos.com/blog/en-sql-null-es-null-vacio-es-vacio

- No es lo mismo vacio que nulo
- 

Se tiene una tabla con nombre y empresa

```sql
    select  nombre, 
            empresa 
    from Estudiantes;
```

- pueden existir datos nulos o vacios 
- el vacio = 
- el nulo = null

Por lo que para buscar se tendria que tomar esto en cuenta:

```sql
    select  * 
    from Estudiantes 
    where   (empresa = ' ' or compania is null)
            and registro > '20150101';
```

Para modificar la tabla y mejorarla se puede:

```sql
    alter table Estudiantes 
    modify  column  empresa
                    varchar (200) default ' ' not null;
```