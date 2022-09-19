# consultas1.sql

## CONSULTAS SQL
![alt text](/images/cuhoo.png)

1. Para visualizar toda la informacion que contiene la tabla `usuario`s se puede incluir con lainstruccion SELECT el caracter '*' o cada uno de los campos de la tabla
`select * from usuario`
![alt text](/images/CONSULTA1.png)

2. Visualizar solamente la identificación del usuario.
`select Identificacion from usuario`
![consulta 2](/images/consulta2%7D.png)

3. si se desea obtener los registros cuya identificacion sean mayoreso iguales a 150, se debe utulizar la clausula WHERE que espicifica las condiciones que deben reunir los registros que se van a seleccionar.

`SELECT` * FROM usuario WHERE Identificación>=`150`
![consulta 3](/images/consulta3.png)


4. si se desea obtener los registros cuyos los apellidos sean Vanegas o Cetina, se debe utilizar el operador IN que especifica los registros que se quieren visualizar de unatabla.
`SELECT apellidos FROM usuario WHERE apellidos IN ('Vanegas','Cetina')`
![consulta 4](/images/consulta4.png)

O se puede utilizar el operador OR.

`SELECT apellidos FROM usuario WHERE apellidos='Vanegas' OR apellidos='Cetina'`
![consulta 4_2](/images/consulta4_2.png)


5. si se desea obtener los registros cuya identificacion sea menor de '110' y la ciudad sea 'Cali', se debe utilizar el operador AND.
`SELECT * FROM usuario WHERE Identificacion<'110' AND ciudad_nac='Cali'`
![consulta 5](/images/consulta5.png)


6. si se desea obtener los registros cuyos nombres empiecen por la letra 'A', se debe utilizar el operador LIKE que utiliza los patrones '%' todos y '_' (caracter).
`SELECT * FROM usuario WHERE nombre LIKE 'A%'`
![consulta 6](/images/consulta6.png)


7. si desea obtener los registros cuyos nombres contengan la letra 'a'.
`SELECT * FROM usuario WHERE nombre LIKE '%a%'`
![consulta 7](/images/consulta7.png)


8. si se desea obtener los registros donde la cuarta letra del nombre sea una 'a'.
`SELECT * FROM usuario WHERE nombre LIKE '___a%'`
![consulta 8](/images/consulta8.png)

9. si se desea obtener los registros cuya identificacion este entre el intervalo 110 y 150, se debe utilizar la clausula BETWEEN, que sirve para espicificar un intervalo de valores.
`SELECT * FROM usuario WHERE Identificación '110` AND '150'
![consulta 9](/images/consulta9.png)


## COMANDO DELETE
### 10. Para eliminar solamente los registro cuya identificacion sea mayor de 130.
`DELETE FROM usuario WHERE identificacion > '130'`

![Consulta10](/images/tabla10.png "Tabla delete users")

![Consulta10.1](/images/tabla2.png "Tabla delete users1")

### 11. Para actualizar la ciudad de nacimiento de Andres Vanegas, cuya informacion es 118.

`UPDATE usuario SET ciudad_nac = 'Manizales' WHERE identificacion='118'`
![Consulta11](/images/tabla_actualizar.png "Tabla actualizar datos")

## INNER JOIN 
permite obtener datos de dos o mas tablas. cuando se realiza la concatenación de las tablas, no necesariamente se deben mostrar 

## TABLA PEDIDOS
![pedidios](/images/tablapedidos.png "Tabla pedidos")

12. Para v1suali7ar los campos identificación, nombre, apellidos de la tabla usuario y nropedido, fecha de compra, fecha de vencimiento y observacion de la tabla pedidos, se debe realizar 1a siguiente instrucción sqL:

`SELECT usuario.Identificacion, usuario.nombre, usuario.apellidos, pedido.nropedido, pedidos.fechaCompra, pedidos.fechaVence, pedidos.observacion FROM usuario INNER JOIN pedidos ON usuario.Identificacion = pedidos.Identificacion`

![consulta12](/images/consulta12.png "consulta12")

13.
