Actividad En Clase: 

Parte 1 – Validación LDAP
1. Ver usuarios: ldapsearch-x -b dc=danse,dc=com
![1](imagenes/LDAPII/1.jpeg)
![3](imagenes/LDAPII/3.jpeg)

2. Probar login: ldapwhoami-x -D "uid=dev5,ou=IT,dc=danse,dc=com" –W
![2](imagenes/LDAPII/2.jpeg)


Parte 2 – Web LDAP
Creacion y validación en http://localhost:9020
![4](imagenes/LDAPII/4.jpeg)


Parte 3 – Pruebas
- Login correcto
![4](imagenes/LDAPII/5.jpeg)
![4](imagenes/LDAPII/6.jpeg)
 
- Login incorrecto
![7](imagenes/LDAPII/7.jpeg)
![8](imagenes/LDAPII/8.jpeg)


Actividad Independiente:

- Explicación de autenticación LDAP
LDAP permite entralizar usuarios en un servidor, por lo que en vez de
tener cuentas locales en cada sistema, las aplicaciones consultan el 
directorio LDAP. Este proceso permite al  usuario ingresa credenciales 
en la aplicación, construir un DN con el uid y la OU correspondiente, 
hacer un bind contra el servidor LDAP con ese DN y la contraseña y permitir
el acceso si es autorizado o rechazarlo en caso de fallo.
 
- Flujo de autenticación 
Usuario
Formulario Web
PHP (ldap_connect + ldap_bind)
Servidor LDAP
OK -> Acceso permitido
FAIL -> Error de autenticación

- Código PHP
![9](imagenes/LDAPII/9.jpeg) 

- Evidencias
![10](imagenes/LDAPII/10.jpeg)
![11](imagenes/LDAPII/11.jpeg)
![12](imagenes/LDAPII/12.jpeg)
![13](imagenes/LDAPII/13.jpeg)
