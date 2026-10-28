entramos a xampp  y aplicamos el comando :
![[data base.png]] Debemos dominar estos 28 comandos 
como se elimina un indice ? 
como se hace una tabla ? 
necesitamos conocimiento para solo consola no se te olvide mirar la grabación del 27/10/26 

---
# COMANDOS
SHOW DATABASES ; esto  es mostrar tabla  y simpre se le pondra punto y coma 
![[data base_.png]]

---
## SEGUNDO COMANDO 
Create database "nombre de la tabla " ; 
![[data - base.png]]

---
### TERCER COMANDO 

drop database "nombre de la tabla"; esta función elimina la tabla 
![[data base -.png]]

---
# APRENDIMOS  A USAR , CREAR Y MOSTRAR LAS TABLAS 

---

# COMO CREAR UNA TABLA POR CONSOLA 

![[-data bases.png]]
AQUI SE creo la tabla con este comando le damos en show tables y aparecerá la tabla en teoría 

---
## CUARTO COMANDO 

show columns from "nombre de la carpeta"; aqui mostrara la tabla la cual hemos creado 

![[base data.png]]

---
# QUINTO COMANDO

alter table "nombre de la tabla  DROP" PRIMARY KEY ; pero ay que tener en cuenta que el  motor no deja ya que sale este error 
![[__DATA.png]]

---
# sexto comando 
alter table "nombre de la tabla"  "add nombre de la columna y especificación" id_rol  int(11);
no dejaba quitar la llave primaria debido a que pusimos AUTO_INCREMENT

---

![[Pasted image 20261027192852.png]]

SIEMPRE que queramos eliminar una llave primaria tenemos que eliminar el auto_increment 
no olvidar que todos los comandos están en XAMPP y que tenemos que usar el otro motor grafico que es DBeaver  para las empresas ya que este es muy viejo es para entender el sistema 
