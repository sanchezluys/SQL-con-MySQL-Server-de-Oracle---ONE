# Revisando conceptos SELECT / INSERT / UPDATE / DELETE

Tomado de:

https://www.aluracursos.com/blog/select-insert-update-delete-sql

## 1. Crear - CREATE

Ejemplo de una BD de libros: 

```sql
    -- usando un dato tipo enum
    CREATE TABLE libros (
        id integer primary key auto_increment,
        titulo text,
        autor text,
        ISBN varchar (50),
        edicion varchar (50),
        editorial varchar(50),
        añoPublicacion year,
        ctdPaginas int,
        genero ENUM ('poesia', 'soneto', 'romance', 'fábula', 'novela', 'cronica', 'cuento', 'ensayo', 'biografia', 'chicklit', 'fantasia', 'distopia', 'ficcion cientifica', 'terror', 'fantastica', 'infantojuvenil', 'young adult', 'suspenso', 'autoayuda', 'negocios', 'tecnologia', 'hq', 'aventura'),
        idioma varchar(50),
        cantidad INT,
        disponible int
    );
```

## 2. Agregar o Insertar - INSERT

Insertando un libro:

```sql
    INSERT INTO libros (titulo, 
                        autor, 
                        isbn, 
                        edicion, 
                        editorial, 
                        añoPublicacion, 
                        ctdPaginas, 
                        genero, idioma, 
                        cantidad, 
                        disponible)
            VALUES ('orgullo y prejuicio', 
                    'jane austen', 
                    '978-8544001820', 
                    'lujo', 
                    'martin claret', 
                    2018, 
                    424, 
                    'romance', 
                    'portugues',
                    2, 
                    2);
```



## 3. Eliminando - DELETE

Eliminando el libro con id=2

```sql
    DELETE from libros WHERE id=2;
```


## 4. Actaulizando - UPDATE

Actualizando un libro existente

```sql
    -- UPDATE libros SET disponible=1 WHERE titulo='El Diario de Anne Frank'; // no esta bien
    UPDATE libros SET disponible=1 WHERE id=19; -- esta si esta bien
```

## 5. Mostarndo los datos - SELECT

```sql
    SELECT * from liBros WHERE genero='poesia' AND disponible>0;
```