# Manual de explotacion
## 1. Introducción y arquitectura
"WillamTech" usa unos módulos ERP que se despliegan mediante el Docker Compose. Está diseñado 
para optimizar flujos de ventas y facturación.

## 2. Guía de instalación y reistalación
Para poder levantar el entorno hay unos pasos en los que tener en cuenta:
- Requisitos previos: verificar que se tiene instalado el Docker y el Compose
- Configuración: hay que definir las variables de entorno
- Ejecutar el comando "docker-compose up -d" (sin las comillas).

## 3. Seguridad y Control de Acceso
Hay que configurar los roles:
- Administrador: acceso total a la configuración y sistema.
- Contable: tiene los permisos para la validación de las facturas y la exportación de los archivos.
- Comercial: gestiona los presupuesto y a los clientes. 

## 4. Procedimiento de Backup e informes
El comando para poder respaldar la base de datos relacional y los almacenes de datos es 
el siguiente: DOCX.

## 5. Flujo Operativo de Facturación e informes
A continucación, detallos el proceso de la interfaz de usuarios:
1. La creación: el usuario registra la transacción en la ERP
2. Renderización: QWEB procesa la plantilla del xml y lo impone en la base de datos. El html que se genera, se guarda en wkhtmlopdf y se generará por último, un archivo pdf que se le entregará al cliente.
