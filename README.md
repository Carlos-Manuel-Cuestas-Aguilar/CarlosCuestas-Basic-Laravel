# Laravel Basico para uso General

<p align="center"><a href="https://laravel.com" target="_blank"><img src="https://raw.githubusercontent.com/laravel/art/master/logo-lockup/5%20SVG/2%20CMYK/1%20Full%20Color/laravel-logolockup-cmyk-red.svg" width="400" alt="Laravel Logo"></a></p>

<p align="center">
<a href="https://github.com/laravel/framework/actions"><img src="https://github.com/laravel/framework/workflows/tests/badge.svg" alt="Build Status"></a>
<a href="https://packagist.org/packages/laravel/framework"><img src="https://img.shields.io/packagist/dt/laravel/framework" alt="Total Downloads"></a>
<a href="https://packagist.org/packages/laravel/framework"><img src="https://img.shields.io/packagist/v/laravel/framework" alt="Latest Stable Version"></a>
<a href="https://packagist.org/packages/laravel/framework"><img src="https://img.shields.io/packagist/l/laravel/framework" alt="License"></a>
</p>

## Requisitos
Laravel es un framework de aplicaciones web con una sintaxis expresiva y elegante. Creemos que el desarrollo debe ser una experiencia agradable y creativa para que sea realmente satisfactorio. Laravel elimina el dolor del desarrollo al facilitar las tareas comunes utilizadas en muchos proyectos web, para poder usarlo se deben tener isntalados ciertos paquetes y son:

### [PHP](https://www.php.net).
  - Thread Safe (TS): Esta versión es más segura para entornos de servidor, ya que está diseñada para manejar múltiples hilos de ejecución, lo cual es importante cuando PHP se ejecuta en un servidor web con Apache o similar.

  - Non-Thread Safe (NTS): Esta versión es más ligera y rápida, pero solo es recomendable cuando se usa PHP en servidores con FastCGI o en entornos de línea de comandos (CLI) donde no se necesitan múltiples hilos. Si estás trabajando con Laravel localmente y en el entorno de desarrollo, puedes optar por esta versión, pero la TS es más comúnmente usada en producción.

- **dentro de la carpeta de php buscar "php.ini", abrirlo y quitar ";" de las siguientes extensiones seleccionar según el tipo de proyecto:**

  - extension=fileinfo: Permite determinar el tipo de archivo según su contenido y no solo por su extensión. Es útil para validar los tipos de archivos cargados en el servidor. Producto/Proyecto: Aplicaciones web que gestionan cargas de archivos, como plataformas de almacenamiento en la nube o sistemas de gestión de contenido.

  - extension=pdo_mysql: Permite a PHP interactuar con bases de datos MySQL a través de PDO (PHP Data Objects). Es más seguro y flexible que las antiguas funciones de MySQL. Producto/Proyecto: Cualquier aplicación que use MySQL como base de datos, como un sistema de gestión de inventarios o un sitio web de comercio electrónico.

  - extension=pdo_sqlite: Proporciona soporte para bases de datos SQLite utilizando PDO. Ideal para bases de datos más ligeras y locales. Producto/Proyecto: Aplicaciones pequeñas o móviles, o sistemas locales de gestión que no necesitan servidores de bases de datos grandes.

  - extension=openssl: Permite la encriptación y seguridad mediante SSL/TLS. Se utiliza para conexiones seguras y encriptación de datos. Producto/Proyecto: Cualquier aplicación que maneje datos sensibles o que requiera una comunicación segura, como sistemas bancarios en línea o tiendas de comercio electrónico.

  - extension=mbstring: Permite trabajar con cadenas de texto multibyte, como caracteres especiales de lenguajes asiáticos (chino, japonés, etc.). Producto/Proyecto: Aplicaciones que gestionan contenido multilingüe, como plataformas de traducción, foros internacionales o cualquier aplicación que maneje diferentes alfabetos.

  - extension=curl: Permite realizar solicitudes HTTP y manejar la comunicación con otros servicios web a través de cURL. Producto/Proyecto: Integraciones con APIs externas, como aplicaciones que obtienen datos de otras plataformas o servicios de pagos.

  - extension=intl: Proporciona soporte para internacionalización e idiomas (formatos de fecha, moneda, etc.), permitiendo la localización de la aplicación. Producto/Proyecto: Aplicaciones globales que necesitan soportar múltiples idiomas, como plataformas de comercio internacional o aplicaciones de contenido diverso.

  - extension=gd: Proporciona herramientas para crear y manipular imágenes en PHP. Permite generar gráficos, redimensionar imágenes, etc. Producto/Proyecto: Aplicaciones de generación de gráficos o imágenes, como sistemas de gestión de contenidos, galerías de fotos, o generadores de miniaturas.

  - extension=zip: Permite trabajar con archivos comprimidos en formato .zip, tanto para descomprimir como para crear archivos zip. Producto/Proyecto: Herramientas de compresión de archivos o cualquier aplicación que permita a los usuarios subir o descargar archivos comprimidos, como servicios de almacenamiento o descarga masiva de archivos.

  - extension=sqlite3: Soporta la base de datos SQLite, una base de datos ligera que no requiere un servidor de base de datos externo. Producto/Proyecto: Aplicaciones locales o móviles que no necesitan un servidor de base de datos completo, como aplicaciones de escritorio o apps móviles pequeñas.

  - extension=pdo_pgsql: Proporciona soporte para la base de datos PostgreSQL a través de PDO. Producto/Proyecto: Aplicaciones que requieren bases de datos PostgreSQL, como proyectos de gestión de datos empresariales o aplicaciones científicas.

  - extension=pdo_odbc: Soporta la conexión a bases de datos mediante ODBC, permitiendo la integración con distintos tipos de bases de datos. Producto/Proyecto: Aplicaciones que deben conectarse a bases de datos empresariales a través de ODBC, como sistemas de gestión empresarial (ERP) o aplicaciones de integración de datos.

  - extension=mysqli: Permite interactuar con bases de datos MySQL utilizando la interfaz MySQLi. Ofrece características más modernas que mysql pero menos flexible que PDO. Producto/Proyecto: Aplicaciones que usan bases de datos MySQL, especialmente cuando se requiere un acceso rápido y sencillo a la base de datos sin las características adicionales de PDO.

  - extension=odbc: Permite la conexión a bases de datos a través de ODBC, proporcionando un acceso más general a una variedad de bases de datos. Producto/Proyecto: Proyectos que necesitan conectarse a diferentes tipos de bases de datos o utilizar bases de datos heredadas en entornos empresariales.

  - extension=ftp: Permite interactuar con servidores FTP para transferir archivos, como subir o descargar archivos desde un servidor remoto. Producto/Proyecto: Aplicaciones que gestionan archivos o permiten transferencias de datos desde o hacia servidores FTP, como sistemas de backup en la nube o aplicaciones de carga de archivos.

### [COMPOSER](https://getcomposer.org/download).
### [Laravel Intaller](https://github.com/laravel/installer).  /*En consola escribir "composer global require laravel/installer" */
### [NODE](https://nodejs.org/es).

## método rápido de instalación de PHP y Composer:
 **Correr consola como administrador**
Set-ExecutionPolicy Bypass -Scope Process -Force; [System.Net.ServicePointManager]::SecurityProtocol = [System.Net.ServicePointManager]::SecurityProtocol -bor 3072; iex ((New-Object System.Net.WebClient).DownloadString('https://php.new/install/windows/8.4'))

`código en línea`.
🔹 **Salida**:
```
Este es un bloque de código sin resaltar.
```
-*- Crear un Proyecto
laravel new example-app

-*-*- Would you like to install a starter kit? [No starter kit]: /* este proyecto es básico, elegiré "none" */
-*-*--none: No instalará ningún kit de inicio. Es ideal si quieres empezar desde cero sin ninguna funcionalidad adicional.
-*-*--breeze: Laravel Breeze es un kit de inicio básico que incluye autenticación (registro, inicio de sesión, restablecimiento de contraseña) y una interfaz de usuario simple utilizando Blade (el motor de plantillas de Laravel) y Tailwind CSS.
-*-*--jetstream: Laravel Jetstream es un kit de inicio más avanzado que incluye más características que Breeze, como autenticación, verificación de correo electrónico, administración de sesiones y equipos (para aplicaciones colaborativas). También ofrece soporte para Livewire o Inertia.js, lo que permite construir aplicaciones más dinámicas sin tener que escribir mucho código JavaScript.

-*-*-Which testing framework do you prefer? [Pest]: /* escoger pest, el mas adecuado y rapido */
-*-*--Pest: Pest es un framework de pruebas más moderno y elegante que se construye sobre PHPUnit, y está diseñado para ser más fácil de usar y entender, con una sintaxis más simple.
-*-*--PHPUnit: PHPUnit es el framework de pruebas estándar en Laravel (y PHP en general). Es ampliamente utilizado y tiene más configuraciones avanzadas, pero su sintaxis puede ser más compleja en comparación con Pest.

-*-*-Which database will your application use? [SQLite]: /*para prueba básica y sin complicaciones escogí SQLite*/
-*-*--sqlite: SQLite es una base de datos ligera que se almacena en un solo archivo. Es ideal para aplicaciones pequeñas o para desarrollo local, donde no necesitas una base de datos compleja.
-*-*--mysql: MySQL es una base de datos relacional muy popular. Es ideal para aplicaciones más grandes o cuando necesitas alta disponibilidad, escalabilidad o características más avanzadas.
-*-*--mariadb: MariaDB es una bifurcación de MySQL, creada por los mismos desarrolladores de MySQL. Es completamente compatible con MySQL, pero tiene algunas mejoras y características adicionales.
-*-*--pgsql: PostgreSQL es una base de datos relacional avanzada, conocida por su rendimiento y características como transacciones ACID, y soporte para consultas complejas. Es útil si necesitas un sistema de base de datos robusto.
-*-*--sqlsrv: SQL Server es una base de datos de Microsoft. Es ideal si estás trabajando en un entorno de Microsoft y necesitas integrarte con otras tecnologías de Microsoft.

-*-*-Would you like to run the default database migrations? (yes/no) [yes]: /* es solo para que corra las migraciones o no*/
-*-*--yes: Laravel ejecutará las migraciones predeterminadas que incluyen tablas como users, password_resets, failed_jobs, etc., dependiendo de las opciones seleccionadas.
-*-*--no: Si eliges "no", Laravel no ejecutará ninguna migración al instalar el proyecto, y serás tú quien maneje la creación de las tablas manualmente o mediante migraciones personalizadas.

-*ejecutar el servicio
Composer run dev

como darle estilos al README:
https://docs.github.com/es/get-started/writing-on-github/getting-started-with-writing-and-formatting-on-github/basic-writing-and-formatting-syntax
