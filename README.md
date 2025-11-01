🍽️ Yola - Aplicación Web de Restaurante

Una aplicación web completa para la gestión de un restaurante. Permite a los administradores gestionar platillos, eventos y ver consumos. Los usuarios pueden registrarse, iniciar sesión y ver la información pública del restaurante.

🛠️ Tecnologías Utilizadas

Backend

PHP: Lenguaje de programación principal.

MySQL: Sistema de gestión de bases de datos.

Arquitectura MVC: Patrón de diseño Modelo-Vista-Controlador implementado de forma nativa.

Active Record: Patrón de diseño para la manipulación de la base de datos (implementación personalizada en models/ActiveRecord.php).

Composer: Gestor de dependencias de PHP.

phpmailer/phpmailer: Para el envío de correos electrónicos (confirmación de cuenta, recuperación).

intervention/image: Librería para el procesamiento y optimización de imágenes.

vlucas/phpdotenv: Para la gestión de variables de entorno.

Frontend

JavaScript (ES6+): Para la interactividad del lado del cliente.

SASS (SCSS): Preprocesador de CSS para estilos.

Gulp: Automatizador de tareas (compilación de SASS, minificación de JS, optimización de imágenes).

Node.js (npm): Gestor de paquetes de frontend y ejecutor de tareas.

💂️ Estructura del Proyecto

📚 Yola (Proyecto Raíz)
├── 📚 classes/                # Clases auxiliares (Email.php, Paginacion.php)
├── 📚 controllers/            # Controladores (lógica de peticiones)
├── 📚 includes/               # Archivos de configuración (app.php, database.php, .env)
├── 📚 models/                 # Modelos de datos (ActiveRecord.php, Usuario.php, Platillo.php)
├── 📚 public/                 # Punto de entrada (index.php) y assets públicos
│   ├── 📚 build/              # Archivos compilados (CSS, JS)
│   └── 📚 img/                # Imágenes optimizadas
├── 📚 src/                    # Archivos fuente de frontend
│   ├── 📚 js/                 # Scripts de JavaScript
│   └── 📚 scss/               # Archivos de SASS
├── 📚 sql/                    # Dump de la base de datos (restaurante_js.sql)
├── 📚 vendor/                 # Dependencias de Composer
├── 📚 views/                  # Vistas y plantillas (HTML/PHP)
│   ├── 📚 admin/              # Vistas del panel de administración
│   ├── 📚 auth/               # Vistas de autenticación (login, registro)
│   ├── 📚 paginas/            # Vistas públicas (inicio, nosotros, etc.)
│   └── 📚 templates/          # Partes reutilizables (header, footer, sidebar)
├── 📝 .htaccess               # Configuración de Apache
├── 📝 Router.php              # Enrutador personalizado
├── 📝 composer.json           # Dependencias de PHP
├── 📝 gulpfile.js             # Configuración de tareas Gulp
└── 📝 package.json            # Dependencias de Node.js


⚙️ Características Principales

Este proyecto se divide en un área pública y un panel de administración:

Área Pública (/)

Inicio: Página de bienvenida.

Autenticación:

Registro de nuevas cuentas.

Confirmación de cuenta por Email.

Inicio de sesión.

Recuperación de contraseña (con token por email).

Páginas Informativas: "Cómo Funciona", "Sobre Nosotros", "Platos".

API de Platillos: Endpoint en /api/platillos para consumir los platillos desde el frontend.

Panel de Administración (/admin)

Dashboard: Vista principal con métricas (en desarrollo).

Gestión de Platillos: CRUD completo (Crear, Leer, Actualizar, Borrar) para los platillos del menú.

Gestión de Eventos: CRUD completo para los eventos del restaurante.

Consumos: Vista de los consumos registrados (en desarrollo).

Usuarios Registrados: Vista de los usuarios registrados en la plataforma.

🏃‍♂️ Cómo Ejecutar la Aplicación

Sigue estos pasos para configurar y ejecutar el proyecto en un entorno local:

Base de Datos:

Importa el archivo sql/restaurante_js.sql en tu gestor de MySQL (phpMyAdmin, MySQL Workbench, etc.) para crear la base de datos y sus tablas.

Variables de Entorno:

Navega a la carpeta includes/.

Renombra (o copia) el archivo .env (si es un template) o edítalo directamente.

Configura tus credenciales de base de datos y del servicio de correo (PHPMailer):

DB_HOST=localhost
DB_USER=tu_usuario_db
DB_PASS=tu_password_db
DB_NAME=restaurante_js

EMAIL_HOST=smtp.mailtrap.io
EMAIL_PORT=2525
EMAIL_USER=tu_usuario_mailtrap
EMAIL_PASS=tu_password_mailtrap


Dependencias de Backend (PHP):

Abre una terminal en la raíz del proyecto y ejecuta:

composer install


Dependencias de Frontend (Node.js):

En la misma terminal, instala las dependencias de Node:

npm install


Compilar Assets de Frontend:

Ejecuta Gulp para compilar los archivos SASS y JS:

npm run dev


(Este comando ejecutará la tarea dev definida en gulpfile.js y package.json).

Servidor Local:

Opción A (Servidor de PHP): La forma más rápida de probar.

php -S localhost:8000 -t public


Opción B (Apache/Nginx): Configura un host virtual (ej. yola.test) que apunte al directorio public/ del proyecto.

Acceso:

Abre tu navegador y visita http://localhost:8000 (o la URL que hayas configurado).
