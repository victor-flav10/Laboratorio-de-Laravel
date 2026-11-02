# Laboratorio-de-Laravel
Siguiendo los pasos de la guia de instalacion de Laravel subida en el sitio virtual, se pudo completar el laboratoria de manera exitosa y bien organizada.


## 📅 Fecha de Ejecución
- **Fecha:** Octubre de 2026

## 👥 Datos del Estudiante (Footer / Presentación)
- **Nombre:** Víctor Flavio
- **Correo:** [Tu correo institucional UTP]
- **Curso:** Desarrollo Web (II Semestre 2026)
- **Instructor del Laboratorio:** Ing. Irina Fong

---

## 📋 1. Requisitos Previos y Ecosistema de Desarrollo
- **Sistema Operativo:** Windows 10/11 (64-bit).
- **Entorno Local (Servidor web):** WampServer (Apache 2.4 / MySQL)[cite: 6].
- **Lenguaje:** PHP versión 8.5.0 (CLI)[cite: 6].
- **Gestor de Dependencias:** Composer (última versión estable)[cite: 6].
- **Node.js & NPM:** Instalado para la compilación de recursos con Vite[cite: 6].
- **Editor de Código:** Visual Studio Code[cite: 6].

### Flujo de Comandos de Instalación y Dependencias:
```bash
# Creación del proyecto Laravel
composer create-project laravel/laravel Laboratorio_Laravel

# Instalación del paquete de autenticación con Bootstrap (laravel/ui)
composer require laravel/ui
php artisan ui bootstrap --auth
npm install
