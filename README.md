📘 Laravel Lab – Login System
👤 Autor: Hilda Acosta

🧰 1. Prerrequisitos del entorno

Para ejecutar este laboratorio se requiere el siguiente ecosistema de desarrollo:

🖥️ Tecnologías base
🐘 PHP >= 8.0
📦 Composer (última versión estable)
🚀 Laravel Installer o creación del proyecto con:
laravel new
composer create-project
🌐 Servidor local
WAMP / XAMPP / Laragon
Apache
🗄️ Base de datos
MySQL / MariaDB en funcionamiento
🧑‍💻 Herramientas recomendadas
Visual Studio Code
🟩 Node.js + NPM (opcional para este laboratorio)
💻 Sistema operativo: Windows

Laravel sigue el patrón MVC (Model - View - Controller):

📁 Models
Representan la lógica de datos
Conectan con la base de datos (Eloquent ORM)
🎮 Controllers
Manejan la lógica del sistema
Conectan modelos con vistas
🖼️ Views
Interfaz del usuario (Blade templates)
🌐 Routes
Definen las URLs del sistema
Conectan peticiones con controladores
🗄️ 4. Base de datos y configuración (.env)
📌 Configuración del archivo .env
DB_CONNECTION=mysql
DB_HOST=127.0.0.1
DB_PORT=3306
DB_DATABASE=lablaravellogin
DB_USERNAME=root
DB_PASSWORD=
📌 Migraciones
php artisan migrate
📌 Resultado de migraciones

Se crearon automáticamente las tablas:

users
password_reset_tokens
cache
jobs
🔐 5. Autenticación (Laravel Breeze)

Se utilizó Laravel Breeze como sistema de autenticación:

composer require laravel/breeze --dev
php artisan breeze:install
⚠️ Nota sobre Node/NPM
npm install && npm run dev

❌ No fue ejecutado debido a problemas de configuración de Node.js en el entorno de desarrollo.
✔ Esto no afecta la funcionalidad backend del sistema.

📸 6. Evidencia del laboratorio

📌 Insertar aquí captura de pantalla del sistema funcionando

Ejemplo:

Pantalla de login
Registro de usuario
Dashboard
🧪 7. Flujo de ejecución del sistema
composer install
cp .env.example .env
php artisan key:generate
php artisan migrate
php artisan serve
🧰 8. Problemas y soluciones
❌ Problema 1: Error de acceso a MySQL (phpMyAdmin)
Causa: contraseña incorrecta para root
Solución: se dejó el campo DB_PASSWORD vacío
❌ Problema 2: Node.js fallando (npm)
Causa: instalación corrupta de Node.js
Solución: se omitió npm temporalmente
❌ Problema 3: Composer en PowerShell
Causa: restricciones de ejecución en Windows
Solución: se utilizó CMD en lugar de PowerShell
📚 9. Referencias
https://laravel.com/docs
https://getcomposer.org/doc/
https://nodejs.org/en/docs
https://stackoverflow.com/questions/tagged/laravel
🎯 Conclusión

Este laboratorio permitió comprender la estructura base de Laravel, el funcionamiento del patrón MVC, la configuración de bases de datos mediante .env, y la implementación de autenticación con Breeze.
