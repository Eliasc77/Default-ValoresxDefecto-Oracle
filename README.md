# Default Valores x Defecto Oracle
####Configuracion de valores x defecto en una tabla de sql, la clausula default permite colocar valores en una tabla que se van visualizar al momento de hacer una consulta a la misma mostrando el valor que le coloquemos por defecto al momento de realizar esta configuracion.

> Clausula Default

```sql
create table libros(
titulo varchar2(40) not null,
autor varchar2(30) default 'Desconocido',
editorial varchar2(40) not null,
precio number (5,2),
cantidad number (3) default 0
);
```

##### Insertamos Datos
```sql
insert into libros values ( 'El quijote', 'Miguel de Cervantes', ' La casa del Libro', 650.00, 10);
insert into libros values ( 'Guerra yPaz', default, 'Mensajero RUSO', 500.00, 5);
-- con la instruccion default nos traera el valor que ya configuramos en caso de no existir autor para ingresar en la tabla libros.
);
```

```sql
select * from libros;
```
 
 | titulo            | autor           |  editorial   |   precio   |    cantidad    |
 | ------------------|:----------------:|---------------:|-----------:|-----------:|
 | El quijote   | Miguel de Cervantes         |  La casa del Libro   |   650.00   | 10  |
 | Guerra yPaz  | Desconocido        |  Mensajero RUSO  |   500.00  | 5  |


___
