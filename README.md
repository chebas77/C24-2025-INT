Implementación y Lineamientos de Base de Datos
5.2 Implementación: Trunk Based Development
Se recomienda usar el enfoque Trunk Based Development para el control de versiones, donde los desarrolladores colaboran en una única rama con un enfoque en ramas de corta duración e integración continua. Esta metodología promueve la integración rápida y continua de cambios, minimizando los problemas de integración.

Convenciones de Nombres y Flujo de Trabajo
Rama Principal (Main Branch)
Nombre: main

Propósito: Es la rama principal donde todos los cambios se unifican. Siempre debe estar desplegable y libre de errores.

Acceso: Todos los desarrolladores tienen acceso de lectura, pero el merge está restringido y solo se realiza a petición.

Ramas de Funcionalidad (Features Branches)
Nombre: feature/<feature-name>

Propósito: Para el desarrollo de nuevas funcionalidades o cambios. Se crean desde main y se fusionan de nuevo en main.

Tiempo de Vida: Pocos días.

Ejemplo: feature/login-system

Ramas de Corrección de Errores (Bugfix Branches)
Nombre: bugfix/<bug-name>

Propósito: Para resolver rápidamente errores o bugs en la rama main.

Tiempo de Vida: Menos de un día.

Ejemplo: bugfix/email-notification-fix

Ramas de Hotfix
Nombre: hotfix/<hotfix-name>

Propósito: Para resolver errores urgentes en producción.

Origen: Se crea a partir de un tag de la rama main y se fusiona con main.

Ejemplo: hotfix/payment-gateway-fix

Ramas de Release
Nombre: release/<version-number>

Propósito: Para preparar la aplicación para producción.

Ejemplo: release/1.2.0

6. Base de Datos
6.1 Objetivo
Establecer los lineamientos para la nomenclatura de bases de datos, esquemas, tablas y otros objetos. Esto servirá como estándar para futuras actualizaciones y desarrollos.

6.2 Lineamientos Generales
Nombres: Se utilizarán letras minúsculas y el estilo de escritura snake_case para separar palabras con guiones bajos (_).

Singularidad: Los nombres serán siempre en singular.

Restricciones: No se permitirán nombres propios ni palabras reservadas (Ej: SYS, UPDATE, SESSION).

Tamaño: Los nombres no deben exceder los 20 caracteres.

Sin artículos ni espacios: Evitar artículos en los nombres y no utilizar espacios.

6.3 Asignación de Nombres a un Esquema de Base de Datos
El esquema debe contener el prefijo del código del departamento seguido por un nombre que distinga al grupo o área.

Ejemplo: grupo_01, grupo_02.

6.4 Asignación de Nombres a Tablas
Si el sistema es modular (Ej: ERP), se usará un prefijo de hasta 4 caracteres que describa el módulo, seguido de un nombre de la tabla.

Ejemplo: mkt_producto, mkt_cliente.

Para proyectos más acotados, el nombre de las tablas será una palabra representativa en singular.

Ejemplo: cliente, paciente, documento_pago.

6.5 Asignación de Nombres a Vistas
Las vistas tendrán el prefijo v_, seguido del nombre de la tabla a la que hace referencia.

Ejemplo: v_cliente, v_orden_pedido.

6.6 Asignación de Nombres a Campos
Se pueden usar entre 1 a 5 palabras, separadas por guiones bajos.

Llave primaria: Prefijo pk_.

Llave secundaria: Prefijo fk_.

Llave compuesta: Mismo formato que las llaves primarias.

Restricción única: Prefijo un_.

6.7 Asignación de Nombres a Otros Objetos
6.7.1 Stored Procedures (SP)
Prefijo: sp_

Ejemplo: sp_actualiza_orden

6.7.2 Paquetes (Package)
Prefijo: paq_

Ejemplo: paq_actualiza_datos_cliente

6.7.3 Triggers
Prefijo: tr_, seguido de:

i para Insert.

u para Update.

d para Delete.

a para Auditoría.

Ejemplo: tr_gestor_i_alumno

6.7.4 Índices
Prefijo: idx_

Ejemplo: idx_ordena_productos_producto_codigo

6.7.5 Funciones
Prefijo: fn_

Ejemplo: fn_calcula_igv
