# Laboratorio #2 – Patrón MVC en Laravel

## Introducción

En este laboratorio se realizó un primer acercamiento al framework Laravel, el cual utiliza el patrón de arquitectura Modelo–Vista–Controlador (MVC).

El objetivo principal fue comprender la estructura del framework, su funcionamiento y la implementación de un sistema de autenticación (login y registro), así como la configuración del entorno de desarrollo.

---

## Objetivo del Laboratorio

- Comprender la arquitectura MVC en Laravel.
- Configurar correctamente un proyecto Laravel.
- Implementar un sistema de autenticación.
- Ejecutar migraciones y trabajar con base de datos.

---

## Arquitectura MVC en Laravel

- **Modelos (Models):** Representan la base de datos.
- **Vistas (Views):** Interfaz visual del usuario.
- **Controladores (Controllers):** Lógica de la aplicación.
- **Rutas (Routes):** Conectan URLs con controladores.

---

## Requisitos Previos

- PHP 8.4.15  
- Composer  
- WampServer  
- SQLite (motor de base de datos utilizado en este proyecto) 
- Visual Studio Code  

---

## Instalación y Configuración

Durante el desarrollo del laboratorio se siguió el siguiente flujo:

```
composer create-project laravel/laravel example-app
cd example-app
php artisan migrate
composer run dev
```

Posteriormente, se instaló el sistema de autenticación utilizando:

```
composer require laravel/ui
npm install
php artisan ui bootstrap --auth
npm install
npm run dev
```

Este flujo permitió configurar correctamente el proyecto y habilitar el módulo de login.

---

## Base de Datos

Se utilizó SQLite como motor de base de datos.

Configuración en el archivo .env:

```
DB_CONNECTION=sqlite
DB_DATABASE=database/laravelprueba.db
```

Migraciones ejecutadas:

```
php artisan migrate
```

Esto creó tablas como:

- users
- cache
- jobs

---

## Respaldo de Base de Datos

Se incluye el archivo:

```
database/laravelprueba.db
```

Este archivo contiene el respaldo completo de la base de datos del laboratorio.

---

## Resultado del Laboratorio

<img width="921" height="486" alt="image" src="https://github.com/user-attachments/assets/d08d7472-8bdc-499a-9e76-b0ff1a284183" />
<img width="921" height="128" alt="image" src="https://github.com/user-attachments/assets/e081218e-f078-443d-86b7-bba04869a998" />
<img width="711" height="652" alt="image" src="https://github.com/user-attachments/assets/2dbba094-8751-4e44-8d44-7d0466c43029" />

---

## Consideraciones Adicionales

### Longitud de cadenas

En la guía del laboratorio se menciona el uso de:

```
Schema::defaultStringLength(191);
```

Este ajuste se utiliza para evitar errores relacionados con la longitud de índices en bases de datos MySQL.

Sin embargo, en este proyecto no fue necesario aplicarlo, ya que se utilizó SQLite como motor de base de datos, el cual no presenta este inconveniente.

### Caché de configuración

En la guía también se menciona el uso de:

```
php artisan config:clear
php artisan config:cache
```

En este laboratorio no fue necesario utilizarlos, ya que no se presentaron problemas de configuración; sin embargo, se recomienda su uso al modificar el archivo .env.

---

## Dificultades y Soluciones

- Configuración de SQLite

  Solución: Crear manualmente el archivo ```.db``` y configurarlo en ```.env```.
  
- Problemas con Composer

  Solución: Verificar la instalación y configuración del entorno.

---

## Referencias

- Documentación oficial de Laravel (https://laravel.com/docs/12.x/installation)
- Guía de laboratorio otorgada por la profesora.
- Video guía otorgado suministrado por la profesora (https://www.youtube.com/watch?v=GZMGyYNq3hE).

---

## Información del estudiante

Este laboratorio ha sido desarrollado por el estudiante de la Universidad Tecnológica de Panamá:
- Nombre: Gabriel Ah Chu
- Correo: gabriel.ahchu@utp.ac.pa
- Curso: Desarrollo de Software 7
- Instructor del Laboratorio: Irina Fong
- Fecha de Ejecución del Laboratorio: 15 de abril de 2026
