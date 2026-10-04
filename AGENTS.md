# proyecto: punto de venta de productos orgánicos

## descripcion: Sistema web para venta de productos orgánicos de la comunidad de san gaspar yagalaxi

## comandos

## stack (tecnologias)
- backend: php
- base de datos: mysql
- frontend: html, css, bootstrap v5 y javascript

## convenciones (como se debe escribir el código)
- Arquitectura modelo-vista-controlador (MVC)
- Consultas SQL siempre parametrizadas (PDO con consultas preparadas)
- Contraseñas con `password_hash()` y `password_verify()`, nunca en texto plano

## Reglas
- Implementar solo lo que se pida
- No modificar archivos de la carpeta docs/ ni AGENTS.md
- No modificar config/database.php
- Seguir los requisitos, el diseño y las tareas de la carpeta del sprint indicado en docs/

## nomenglatura
- Clases: PascalCase (`UsuarioController`)
- Archivos de clases: igual que la clase (`UsuarioController.php`)
- Métodos y variables: camelCase (`obtenerUsuario`)
- Constantes: UPPER_SNAKE_CASE (`MAX_INTENTOS_LOGIN`)
- Tablas y columnas de MySQL: snake_case (`fecha_creacion`)
- Nombres en español, sin abreviaturas

## Documentación
- Comentarios en español cada línea de código
- Actualizar el README cuando se agregue un módulo nuevo

