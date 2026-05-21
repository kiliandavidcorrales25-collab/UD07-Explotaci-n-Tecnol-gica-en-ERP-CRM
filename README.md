# Manual de WillmanTech S.L.

## 1. Introducción y Arquitectura

El documento explica el procedimiento de mantenimiento y administración del sistema ERP/CRM que a sido usado en la empresa WillmanTech S.L. El sistema es desplegado con contenedores Docker utilizando Docker Compose, Los modulos activos para el funcionamiento del ERP son:

- Facturación
- ventas
- inventario

# 2. Guía de Instalación y Reinstalación

Para desplegar correctamente el entorno es necesario disponer previamente de Docker, Docker Compose y Git instalados en el sistema operativo.


# 3. Seguridad y Control de Acceso

El sistema implementa un modelo de seguridad basado en roles y privilegios para de proteger la información de la empresa y limitar el acceso a los recursos autorizados para cada usuario. Se han configurado tres perfiles principales de acceso; administrador, contable y comercial. 
- Administrador: El rol de administrador dispone todos los permisos, pudiendo gestionar a otros usuarios, 

- Contable: tiene los permisos específicos relacionados con las facturas, gestión de impuestos e informes financieros.

- Usuario comercial: Solo tiene acceso a funciones relacionadas con clientes, presupuestos y pedidos de venta.

Para reforzar la seguridad del sistema, las contraseñas cumplen una política de al menos ocho caracteres, comibnacion de letras mayúsculas y números y renovación cada cierto tiempo del a contraseña. Además, el sistema restringe el acceso a información según los privilegios de cada usuario.


# 6. Conclusión

La implantación del ERP/CRM en WillmanTech S.L. tendra una infraestructura centralizada, escalable para la gestión. El uso de Docker facilita el mantenimiento del entorno, mientras que las plantillas QWeb y los demas garantizan la automatización. La documentación técnica ha sido creada siguiendo las recomendaciones del estándar ISO/IEC/IEEE 26514:2022.
