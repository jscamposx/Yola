# Yola - Aplicación Web de Restaurante

Yola es una aplicación web completa para la gestión de restaurantes, permitiendo administrar platillos, eventos y usuarios, así como ofrecer una experiencia pública para clientes con información general del restaurante.

## Tecnologías Utilizadas

### Backend

* **PHP**: Lenguaje principal.
* **MySQL**: Sistema de gestión de bases de datos.
* **Patrón MVC**: Implementación nativa del patrón Modelo-Vista-Controlador.
* **Active Record**: Implementación personalizada para la manipulación de datos.
* **Composer**: Gestión de dependencias.
* **phpmailer/phpmailer**: Envío de correos electrónicos.
* **intervention/image**: Procesamiento y optimización de imágenes.
* **vlucas/phpdotenv**: Manejo de variables de entorno.

### Frontend

* **JavaScript (ES6+)**
* **SASS (SCSS)**
* **Gulp** para compilación, minificación y optimización.
* **Node.js (npm)** para gestión de paquetes.

## Estructura del Proyecto

```
Yola/
├── classes/                # Clases auxiliares
├── controllers/            # Controladores
├── includes/               # Configuración y entorno
├── models/                 # Modelos y ActiveRecord
├── public/                 # Punto de entrada y assets
│   ├── build/              # Archivos compilados
│   └── img/                # Imágenes optimizadas
├── src/                    # Código fuente frontend
│   ├── js/
│   └── scss/
├── sql/                    # Dump de base de datos
├── vendor/                 # Dependencias de Composer
├── views/                  # Plantillas y vistas
│   ├── admin/
│   ├── auth/
│   ├── paginas/
│   └── templates/
├── .htaccess
├── Router.php
├── composer.json
├── gulpfile.js
└── package.json
```

## Características

### Área Pública

* Registro y autenticación de usuarios.
* Confirmación de cuenta vía correo.
* Recuperación de contraseña mediante token.
* Páginas informativas (Inicio, Nosotros, Menú, etc.).
* API pública para consumo de datos de platillos.

### Panel de Administración

* Dashboard general.
* CRUD completo para platillos y eventos.
* Lista de usuarios registrados.
* Gestión de consumos (en desarrollo).

## Instalación y Configuración

### 1. Base de Datos

Importar el archivo ubicado en:

```
sql/restaurante_js.sql
```

### 2. Variables de Entorno

Editar `.env` en `includes/` con los valores correspondientes:

```
DB_HOST=localhost
DB_USER=usuario
DB_PASS=password
DB_NAME=restaurante_js

EMAIL_HOST=smtp.mailtrap.io
EMAIL_PORT=2525
EMAIL_USER=usuario_mailtrap
EMAIL_PASS=password_mailtrap
```

### 3. Dependencias del Backend

```
composer install
```

### 4. Dependencias del Frontend

```
npm install
```

### 5. Compilación de Assets

```
npm run dev
```

### 6. Ejecución del Servidor Local

```
php -S localhost:8000 -t public
```

## Acceso a la Aplicación

Abrir en navegador:

```
http://localhost:8000
```

## Licencia

Este proyecto se encuentra bajo licencia de uso personal y académico. Ajustar según necesidades.
