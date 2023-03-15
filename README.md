# Proyecto de prueba - Liquibase

### Para el punto 3, 5, 8:
Utilizar la configuracion: **changeLogFile=./changesets/db.changelog-master.xml** 

Y la base de datos **jdbc:mysql://localhost:3306/cap_liquibase_test**
### Para el punto 4, 6, 7:
Utilizar la configuracion: **changeLogFile=./changesets/dbtest.changelog-master.xml**

Y la base de datos **jdbc:mysql://localhost:3306/cap_liquibase**

## Punto 3
![Image Text](/imgs/1.png)

***

## Punto 4
![Image Text](/imgs/3.png)

*** 

## Punto 5
![Image Text](/imgs/4.png)

***

## Punto 6
Se utilizo el comando
```
liquibase rollbackCount 2
```
Para revertir la los datos y para eliminar la tabla

![Image Text](/imgs/5.png)

***

## Punto 7
Se crea el siguiente *Procedure* 
```
CREATE PROCEDURE GetAllMaterias()
BEGIN
	SHOW TABLES;
END;
```
Contenido en el archivo **changesets/db.changelog-0.0.0.3.xml**

![Image Text](/imgs/6.png)

***

## Punto 8
Se crea el siguiente archivo: **changelogs/db.changelog.sql.xml**

***

## Punto 9
Se crear el siguiente archivo: **diffchangelogs/diff.changelog.xml**

Con el comando
```
liquibase diff-changelog --changelog-file=diffchangelogs/diff.changelog.xml
```
> tener la configuracion: ***referenceUrl: jdbc:mysql://localhost:3306/cap_liquibase_test***