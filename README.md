# sqlite

### Update

El update se usa para actualizar un registro ya hecho en una base de datos. <br>Se usan las mismas sentencias que se usan en la mayoria de los sistemas gestores de bases de datos relacionales. <br>Ejemplo: <br> update users set email= "jmberdugo50@misena.edu.co" where userid=2;

### Schema

El comando ".schema" nos permite saber como construimos la tabla en la base de datos.

### Date and Time Functions

Son funciones que nos permiten trabajar con la fecha y el tiempo, las funciones usadas son: <br>-date()<br>-time()<br>-datetime()<br>-julianday()<br>-strftime()

### Primary key constraint

La primary key es el atributo que va a identificar nuesta tabla, en este caso tambien es como en la mayoria de los sistemas gestores. <br>Ejemplo: <br>create table employees(employeeid int primary key);

### Not null constraint

Este nos indica que dentro de la tabla el atributo no puede ser de tipo nulo. <br>Ejemplo: <br> employees(employeeid int not null);

### Unique constraint

Nos indica que el campo tiene que ser unico, que no pueden haber dos campos en el mismo atributo que sean iguales. <br>Ejemplo: <br> employees(employeeid int unique);

### Default constraint

Este nos ayuda a poner un valor por defecto a cada registro donde no se especifique el valor del atributo. <br>Ejemplo: <br> employees(employee_status int defult "married");

### Check constraint

Nos asegura que al ingresar un registro en un atributo se cumpla un condicional que hayamos indicado <br>Ejemplo: <br> employees(employeeid int, check(employeeid > 0));

### Alter table

Nos permite modificar la tabla <br>Ejemplo: <br> alter table employees add column age int not null;

### Drop y delete

Los dos nos sirven para eliminar, drop para eliminar estructuras y delete para borrar registros <br>Ejemplos: <br>drop table employees; <br> delete from employees where employeeid = 2;

### Backup y restore

Nos ayudan en que tal sea el caso de que se borre la informacion de la base de datos tengamos un respaldo para implementarla de nuevo y asi ahorrarnos el trabajo de comenzar desde cero <br>Ejemplo:<br>*Hacer backup* <br> 1- .dump <br> 2- .output employees_backup.txt <br> 3- .dump <br> 4- .output stdout <br> 5- .dump <br> *Hacer restore* <br> 1- .read employees_backup.txt <br> 2- .dump
