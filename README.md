# Manual de WillmanTech S.L.

## 1. Introducción y Arquitectura

El documento explica el procedimiento de mantenimiento y administración del sistema ERP/CRM que a sido usado en la empresa WillmanTech S.L. El sistema es desplegado con contenedores Docker utilizando Docker Compose, Los modulos activos para el funcionamiento del ERP son:

- Facturación
- ventas
- inventario

# 2. Guía de Instalación y Reinstalación

Para la instalacion del sistema de wilmanTechgS.L. es neceasrio tener previemante isntalado el docker compose y Git en el ordemnnador o servidor donde se vayan a ejecutar.  El sistema funciona utlizandio contenedores de docker, lo que hace que los servidores esten organizados de forma clara y seperados correctamente para facilitar la isntalacion de facutras y tareas necesarias para la empresa.

# 3. Seguridad y Control de Acceso

El sistema implementa un modelo de seguridad basado en roles y privilegios para de proteger la información de la empresa y limitar el acceso a los recursos autorizados para cada usuario. Se han configurado tres perfiles principales de acceso; administrador, contable y comercial. 
- Administrador: El rol de administrador dispone todos los permisos, pudiendo gestionar a otros usuarios, 

- Contable: tiene los permisos específicos relacionados con las facturas, gestión de impuestos e informes financieros.

- Usuario comercial: Solo tiene acceso a funciones relacionadas con clientes, presupuestos y pedidos de venta.

Para reforzar la seguridad del sistema, las contraseñas cumplen una política de al menos ocho caracteres, comibnacion de letras mayúsculas y números y renovación cada cierto tiempo del a contraseña. Además, el sistema restringe el acceso a información según los privilegios de cada usuario.

# 4 Procedimiento de Backup y Restauración

Las copias de seguridad son fundamentales para evitar periddas de infromacion en la empresa, por fallos en sitemas, cortes de luz o otros posibles casos. Por ello toda la inframacion que tenga que ver con los clientes , facutras, producto y operaciones comerciales, se almacenan en una base de datos dentro de odoo, por lo que es necesario realizar resplados de manera periodica en la base de datos

# 5 Flujo Operativo de Facturación e Informes

El proceso de facutracion dentro del ERP empieza cuando el usuario accede al modulo de ventas y crea una nueva facutra asociada a un cliente que se ha registrado previamente en el sistema. Durante el proceso se añaden los productos o servidoress que el cliente va a comprar, y los precios unitarios de estos.

Automaticamente, el ERP calucla los impuestos, subtotales y el importe total de la facutra, una vez se ha validado, toda la informacion se guarda en la base de datos y puede sr reutlizada para otros informes, cuando todo el proceso temrina el usaurio puede imrpimir la facutra con la plantailla de Qweb, escrita en xml, pdf etc.. Estaplantilla tendra las instrucioens que mouestran la infroamcion guardada en la base de datos.

El orden seria:

Base de datos -> plantilla Qweb -> Html -> PDF

# 6. Conclusión

La implantación del ERP/CRM en WillmanTech S.L. tendra una infraestructura centralizada, escalable para la gestión. El uso de Docker facilita el mantenimiento del entorno, mientras que las plantillas QWeb y los demas garantizan la automatización. La documentación técnica ha sido creada siguiendo las recomendaciones del estándar ISO/IEC/IEEE 26514:2022.
