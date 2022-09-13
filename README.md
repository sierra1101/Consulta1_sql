# Consulta #1 Sql

## CONSULTAS SQL


1. Para visualizar toda la información que contiene la tabla `usuario` se puede incluir con la instrucción SELECT el caracter `*` o cada una de los campos de la tabla 

- `SELECT * FROM usuario`

![Consulta1](img/tabla_usuario.png "Tabla usuario")

2. Seleccionar o visualizar solamente la identificación del usuario.

- `SELECT Identificación FROM usuario`

![Consulta2](img/tabla_identificacion.png "Tabla Identificacion")

3. Si se desea obtener los registros cuya identificacion sean mayores o iguales a 150, se debe utilizar la consulta WHERE que especifica las condiciones que deben reunir los registros que se van a seleccionar-

- `SELECT * FROM usuario WHERE identificacion >= 150`

![Consulta3](img/tabla_mayorque.png "Tabla Mayor o igual que")

4. Si se desea obtener los registros cuyo sus apellidos sean Vanegas o Cetina, se debe utilizar el operador IN que especifica los registros 
- `SELECT apellidos FROM usuario WHERE apellidos IN ('Vanegas', 'Cetina')`

![Consulta4](img/tabla_apellidos1.png "Tabla Apellidos1")

### O se puede utilizar el operador OR.

- `SELECT apellidos FROM usuario WHERE apellidos='Vanegas' OR apellidos='Cetina'`

![Consulta4.1](img/tabla_apellidos2.png "Tabla Apellidos2")

5. Si se desea obtener los registros cuya identificacion sea menor de '110' y la ciudad sea 'Cali', se debe utilizar el operador AND.

- `SELECT * FROM usuario WHERE identificacion < 110 AND ciudad_nac='Cali'`

![Consulta5](img/tabla_iden-ciudad.png "Tabla Apellidos2")

6. Si se desea obtener los registros cuyos nombres empiecen por la letra 'A', se debe usar el operador LIKE que usa los patrones '%' (todos) y '_' (caracter).

`SELECT * FROM usuario WHERE nombre LIKE 'A%'`

![Consulta6](img/tabla_nombreA.png "Tabla nombreA")