🗂️ Convenciones y Recomendaciones para el Desarrollo
Trunk Based Development:
Main Branch:

Nombre: main

Propósito: Es la rama principal donde todos los cambios se unifican. Siempre debe estar desplegable y libre de errores.

Acceso: Todos los desarrolladores tienen acceso de lectura, pero el merge está restringido y solo se realiza a solicitud.

Features Branches:

Nombre: feature/<feature-name>

Propósito: Para el desarrollo de nuevas funcionalidades. Se crean desde la rama principal y se fusionan de vuelta con la main.

Tiempo de vida: Algunos días.

Ejemplo: feature/login-system

Bugfix Branches:

Nombre: bugfix/<bug-name>

Propósito: Para resolver errores en la rama main.

Tiempo de vida: Menos de un día.

Ejemplo: bugfix/email-notification-fix

Hotfix Branches:

Nombre: hotfix/<hotfix-name>

Propósito: Para errores urgentes en producción. Se bifurca de un tag del main y se unifica con main una vez resuelto.

Ejemplo: hotfix/payment-gateway-fix

Release Branches:

Nombre: release/<version-number>

Propósito: Para preparar un pase a producción, obtenida de la main.

Ejemplo: release/1.2.0

🔍 Lineamientos para la Nomenclatura de Bases de Datos
Generalidades:
Nombres en minúsculas.

Usar snake_case (guión bajo) para separar palabras.

Evitar palabras reservadas, como SYS, UPDATE, etc.

Limitar los nombres a 20 caracteres.

Utilizar nombres singulares.

Asignación de Nombres a Esquemas de Bases de Datos:
Prefijo del código de departamento seguido de una palabra distintiva.

Ejemplo: grupo_01, grupo_02.

Asignación de Nombres a Tablas:
Para sistemas modulares, usar un prefijo de 4 caracteres seguido de la palabra representativa.

Ejemplo: mkt_producto, mkt_cliente.

Para proyectos acotados, el nombre debe ser descriptivo y en singular. Ejemplo: cliente, orden_pedido.

Usar el prefijo tmp_ para tablas temporales. Ejemplo: tmp_orden_pedido.

Asignación de Nombres a Vistas:
Prefijo v_ seguido del nombre representativo de la vista.

Ejemplo: v_productos_disponibles.

Asignación de Nombres a Campos:
Usar uno o más términos separados por guión bajo (no más de 5 palabras).

Llave primaria: Prefijo pk_.

Llave secundaria: Prefijo fk_.

Llave compuesta: Igual que la primaria.

Unique constraint: Prefijo un_.

Asignación de Nombres a Otros Objetos:
Stored Procedures (SP): Prefijo sp_, seguido del esquema y la acción. Ejemplo: sp_actualiza_orden.

Paquetes (Packages): Prefijo paq_, seguido del propósito del paquete. Ejemplo: paq_actualiza_datos_cliente.

Triggers: Prefijo tr_, seguido de tipo (i = Insert, u = Update, d = Delete, a = Auditoría) y la tabla. Ejemplo: tr_gestor_i_alumno.

Índices: Prefijo idx_, seguido de la función y la tabla. Ejemplo: idx_ordena_productos_producto_codigo.

Funciones: Prefijo fn_, seguido del esquema y la acción. Ejemplo: fn_calcula_igv.