# Docker de MySQL para el Bases de Datos 1 - 2025

Este repositorio se creo para ejecutar MySQL + PhpMyAdmin desde docker sin la necesidad de instalar todo localmente.

## ¿Qué incluye?

- MySQL: El programa que guarda y maneja tus bases de datos
- PhpMyAdmin: Una página web que te permite ver y modificar tu base de datos de forma visual (sin escribir código)
- Datos de ejemplo: El proyecto genera información falsa automáticamente para que practiques

## Requisitos

Solo necesitas instalar Docker en tu computadora. Docker es un programa gratuito que puedes descargar de dos formas:

- **Docker Desktop**: Tiene una interfaz visual (ventanas y botones) - Recomendado para principiantes
- **Docker desde consola**: Solo para usar con comandos de texto

Puedes descargar Docker desde: https://www.docker.com/get-started

## Levantar docker-compose

**Opcion 1**: Levantar docker-compose desde consola

1. Abre la consola (Terminal en Mac/Linux, CMD o PowerShell en Windows)
2. Ve a la carpeta del proyecto usando el comando `cd` seguido de la ruta donde guardaste este proyecto
3. Ejecutar este comando 

```bash
docker-compose up -d
```

**Opcion 2**: Usar `docker-compose.yaml`

1. Clickear en **Run all services** en la seccion de `services` 

**Cuando ejecutas estos pasos, Docker hace lo siguiente automáticamente:**

- ✅ Crea contenedores (las "cajas" donde viven MySQL y PhpMyAdmin)
- ✅ Descarga las imágenes necesarias (plantillas de programas)
- ✅ Crea volúmenes (espacios para guardar información)
- ✅ Ejecuta un programa que genera datos falsos para que practiques con la base de datos

## Como acceder a PhpMyAdmin
Phpmyadmin es un gestor de bases de datos que te permite, revisar y modificar las tablas, hacer consultas SQL y agregar registros.

Para acceder, al levantar el contendor acceder a:
```bash
http://localhost:8080
```

**Credenciales**

**Usuario**: root<br>
**Contraseña**: root

**Informacion adicional**

Puerto de MySQL: **3306**

## Detener contenedores

### Para detener TODO y borrar los datos:

Si quieres apagar MySQL y PhpMyAdmin Y BORRAR TODOS LOS DATOS, usa este comando:

```bash
docker-compose down -v
```

>[!WARNING] IMPORTANTE
>Este comando borra toda la información de la base de datos. La próxima vez que inicies el proyecto, se generarán datos nuevos automáticamente.

### Para solo detener temporalmente (sin borrar datos):

Si solo quieres pausar el proyecto pero mantener tus datos, usa estos comandos:

```bash
docker-compose stop
```

**Volver a iniciarlo**

```bash
docker-compose start
```

**Para Reiniciarlo**

```bash
docker-compose restart
```