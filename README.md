# Laboratorio-de-Laravel
Siguiendo los pasos de la guía de instalación de Laravel subida en el sitio virtual, se pudo completar el laboratorio de manera exitosa y bien organizada.


## 📅 Fecha de Entrega
- **Fecha:** 26 de octubre de 2026

## 👥 Datos
- **Nombre:** Victor Flavio
- **Correo:** victor.flavio@utp.ac.pa
- **Curso:** Desarrollo Web (II Semestre 2026)
- **Instructor del Laboratorio:** Ing. Irina Fong

---

## 1. Requisitos Previos y Ecosistema de Desarrollo
- **Sistema Operativo:** Windows 11 (64-bit).
- **Entorno Local (Servidor web):** WampServer (Apache 2.4 / MySQL)
- **Lenguaje:** PHP versión 8.5.0 (CLI)
- **Gestor de Dependencias:** Composer (última versión estable)
- **Node.js & NPM:** Instalado para la compilación de recursos con Vite
- **Editor de Código:** Visual Studio Code

### Flujo de Comandos utilizados en la Instalación de Laravel y Dependencias:
```bash
# Creación del proyecto Laravel
composer create-project laravel/laravel Laboratorio_Laravel

# Instalación del paquete de autenticación con Bootstrap (laravel/ui)
composer require laravel/ui
php artisan ui bootstrap --auth
npm install
```
---

## 2. Introducción y Arquitectura MVCBreve explicación de cómo Laravel implementa el Modelo-Vista-Controlador (MVC) en este laboratorio:
- **Modelos (app/Models/):** Gestionan la interacción con la base de datos (por ejemplo, el modelo User para la autenticación).
- **Vistas (resources/views/):** Interfaces de usuario construidas con plantillas Blade y estilos de Bootstrap (vistas de auth/login.blade.php, auth/register.blade.php, etc.).
- **Controladores (app/Http/Controllers/):** Lasan la lógica entre los modelos y las vistas (ej. Auth/LoginController, HomeController).
- **Rutas (routes/web.php):** Define los endpoints de la aplicación y asigna los middlewares de autenticación.
---

## 3. Evidencia Visual
<img width="1122" height="738" alt="Screenshot 2026-11-03 174552" src="https://github.com/user-attachments/assets/fe979a10-c765-47db-be67-6dc783bc8460" />
<i><small> img 1: Esta imagen muestra algunos de los  comandos ejecutados en el IDE de VS Code </small></i> 
<br></br>
<img width="1535" height="697" alt="Screenshot 2026-11-01 205719" src="https://github.com/user-attachments/assets/3c27fc68-363e-4f89-89b7-c1ac15564edb" />
<i><small> img 2: Esta imagen muestra la pagina de login/register de Laravel </small></i> 
<br></br>
<img width="1453" height="473" alt="Screenshot 2026-11-01 004506" src="https://github.com/user-attachments/assets/ae0362fa-18ad-42b0-9380-93f6be311fa8" />
<i><small> img 3: En esta imagen de puede ver el registro completo y ya logueado  </small></i> 
<br></br>

---

## 4. Configuración de la Base de Datos y Migraciones
<img width="1061" height="628" alt="Screenshot 2026-11-03 183224" src="https://github.com/user-attachments/assets/8c18d7f8-0c8c-473a-bfd3-dc1b5e4e7498" />
<i><small> img 4: Cofiguraciones usadas para correr la base de datos </small></i> 
<br></br><br></br>

- La  copia de la base de datos se encuentra en la carpeta /backup (/Laboratorio_Laravel/database/backup) entre los archivos subidos en el repositorio

---
## 5. Dificultades Encontradas y Soluciones Aplicadas

Durante el desarrollo del laboratorio se presentaron y resolvieron los siguientes retos técnicos:<br></br>
**Dificultad 1:** Conflicto de versión global de PHP en las Variables de Entorno del Sistema (el terminal apuntaba por defecto a PHP 8.0.30 en lugar de PHP 8.5.0, generando incompatibilidades).
**Solución:** Se limpiaron las rutas antiguas en el Path de las Variables de Sistema de Windows y se forzó/priorizó la ruta de PHP 8.5.0 (C:\wamp64\bin\php\php8.5.0). Además, se comentó la extensión incompatible de Xdebug en el php.ini activo.
Tuve que eliminar la verion PHP 8.0.30 en modo global y forzar el PATH de PHP 8.5.0.
<br></br>
**Dificultad 2:** Error de conexión a la base de datos ("No connection could be made because the target machine actively refused it") al intentar correr las migraciones.   
**Solución:** Se verificó que los servicios de WampServer estuvieran activos (ícono en verde) y se creó manualmente la base de datos vacía llamada laboratorio_laravel a través de phpMyAdmin.   <br></br>

**Dificultad 3:** Error de sintaxis en claves largas en las tablas de trabajos ("SQLSTATE[42000]: Syntax error or access violation: 1071 Specified key was too long; max key length is 1000 bytes en la tabla failed_jobs"). 
**Solución:** Se ajustó la longitud de los campos de cadena compuestos en la migración de failed_jobs (reduciendo connection y queue a un tamaño controlado de 191), permitiendo que el índice se creara exitosamente dentro del límite de MySQL, ademas de comentar una línea dentro del bloque de jobs que daba problemas relacionados al tamaño de cadenas </br>

<img width="830" height="621" alt="imagen" src="https://github.com/user-attachments/assets/4e7f8490-d92e-4a4c-b8ac-dd73b639a799" /></br>
<i><small> img 5: Prueba tomado del propio codigo y sus cambios arriba documentados </small></i>
<br></br>

---

## 6. Puntos de Referencia y Bibliografía
- **Documentación Oficial de Laravel: Laravel Documentation - Authentication & Migration**
- **Manual de PHP: PHP: Hypertext Preprocessor Manual**
- **Guía de Laboratorio UTP: Apuntes y lineamientos del curso de Desarrollo Web del II Semestre 2026 por la Ing. Irina Fong.**
