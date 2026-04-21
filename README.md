#  Laravel Lab – Login System

##  Autor
Hilda Itzel Acosta Santana

---

#  1. Objetivo del laboratorio

El objetivo de este laboratorio fue implementar un sistema básico de autenticación utilizando Laravel, comprendiendo el uso del patrón MVC, la configuración de base de datos, la ejecución de migraciones y la integración del frontend mediante Vite.

---

#  2. Arquitectura MVC en Laravel

Laravel utiliza el patrón **MVC (Model - View - Controller)**, el cual organiza el código de la siguiente manera:

##  Models

* Representan la estructura de los datos.
* Se conectan con la base de datos mediante Eloquent ORM.

##  Controllers

* Contienen la lógica del sistema.
* Procesan las solicitudes del usuario y devuelven respuestas.

##  Views

* Interfaz gráfica del usuario.
* Se desarrollan con Blade (motor de plantillas de Laravel).

##  Routes

* Definen las URLs del sistema.
* Conectan las peticiones con los controladores.

---

#  3. Prerrequisitos del entorno

* PHP >= 8.0
* Composer
* Node.js (npm)
* Laravel
* WAMP (Apache + MySQL)
* Visual Studio Code
* Sistema operativo Windows

---

# 4. Instalación del proyecto

```bash
laravel new labLaravelLogin1
cd labLaravelLogin1
```

---

# 5. Configuración de Base de Datos

##  Archivo `.env`

```env
DB_CONNECTION=mysql
DB_HOST=127.0.0.1
DB_PORT=3306
DB_DATABASE=lablaravellogin1
DB_USERNAME=root
DB_PASSWORD=
```

##  Migraciones

```bash
php artisan migrate
```

###  Tablas generadas:

* users
* password_reset_tokens
* cache
* jobs
* migrations

---

#  6. Ejecución del sistema

## Backend (Laravel)

```bash
php artisan serve
```

## Frontend (Vite)

```bash
npm install
npm run dev
```

## Alternativa con Composer

```bash
composer run dev
```

---

# 📸 7. Evidencia del laboratorio
<img width="1894" height="992" alt="Captura de pantalla 2026-04-21 120708" src="https://github.com/user-attachments/assets/b6694877-dea2-4a80-b389-d7f7f3fc0a54" />
<img width="1917" height="1023" alt="Captura de pantalla 2026-04-21 120919" src="https://github.com/user-attachments/assets/f320b2f7-c68b-4244-9c2f-1759c86baa63" />
<img width="1897" height="996" alt="Captura de pantalla 2026-04-21 115448" src="https://github.com/user-attachments/assets/f71afcbf-4f04-4982-b6a9-77dd6ee04e47" />




* Pantalla de Login
* Registro de usuario
* Dashboard phpmyadmin

---

#  8. Flujo de funcionamiento

1. Usuario se registra
2. Datos se almacenan en la base de datos
3. Usuario inicia sesión
4. Laravel valida credenciales
5. Acceso al dashboard

---

# 9. Base de Datos (Backup)

Se realizó un respaldo de la base de datos utilizada en el laboratorio.

 Ubicación sugerida en el repositorio:

```
/database/backup/lablaravellogin1.sql
```

---

#  10. Dificultades y soluciones

## ❌ Problema 1: Error con npm (npm-prefix.js)

* **Causa:** instalación corrupta de Node.js
* **Solución:** reinstalación y corrección manual del archivo `npm.cmd`

---

## ❌ Problema 2: Error ENOENT con PHP en npm

* **Causa:** npm ejecutando PHP incorrectamente
* **Solución:** configurar:

```bash
npm config set script-shell "C:\\Windows\\System32\\cmd.exe"
```

---

## ❌ Problema 3: PowerShell bloqueando Composer

* **Causa:** restricciones de ejecución de scripts
* **Solución:** usar CMD o:

```powershell
cmd /c composer run dev
```

---

## ❌ Problema 4: Error de conexión a MySQL

* **Causa:** servicio MySQL apagado o base de datos inexistente
* **Solución:** iniciar WAMP y crear la base de datos en phpMyAdmin

---

#  11. Referencias

* Video de YouTube: Clase de Laravel – Profesora Irina Fong
* Inteligencia Artificial: ChatGPT (apoyo en resolución de errores y configuración)
* Documentación oficial de Laravel: https://laravel.com/docs

---

#  12. Conclusión

Este laboratorio permitió aplicar conocimientos fundamentales del desarrollo web con Laravel, incluyendo la arquitectura MVC, la gestión de base de datos mediante migraciones y la implementación de autenticación con Laravel Breeze. Además, se adquirió experiencia resolviendo problemas reales de configuración en el entorno de desarrollo.

---
