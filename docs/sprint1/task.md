# Tareas del Sprint 1: login y cuentas de usuario

Reglas: hacer una tarea a la vez, probarla en el navegador y hacer commit antes de pasar a la siguiente.

## 1. Preparación
- [ ] 1.1 Crear la estructura de carpetas MVC (models, views, controllers, public)
- [ ] 1.2 Crear el archivo de configuración de la base de datos .env en la carpeta raiz del proyecto y la conexión con PDO (config/database.php)
- [ ] 1.3 Crear el archivo .gitignore (excluir config/database.php y .env)

## 2. Base de datos
- [ ] 2.1 Conectar la aplicación mediante PDO a la base de datos existente y utilizar la tabla `usuarios` ya creada. No crear, modificar ni eliminar la base de datos ni sus tablas.
- [ ] 2.2 Insertar el administrador inicial en la tabla `usuarios` existente solo si no existe ya; obtener sus datos de configuración y guardar su contraseña con `password_hash()`.

## 3. Modelo
- [ ] 3.1 Crear `Usuario.php` con los métodos: buscarPorCorreo, crear, editar, desactivar y listar (Requisitos 1 y 3)


## 4. Inicio y cierre de sesión
- [ ] 4.0 Crear public/index.php como punto de entrada y dirigir al usuario al login
- [ ] 4.1 Crear la vista `login.php` con formulario, Bootstrap 5 y campos en rojo cuando falten (Requisito 1)
- [ ] 4.2 Crear `AuthController.php` con el método de login usando `password_verify()` (Requisito 1)
- [ ] 4.3 Mostrar el mensaje "Correo o contraseña incorrectos" y bloquear cuentas desactivadas (Requisito 1)
- [ ] 4.4 Crear el cierre de sesión que destruye la sesión y regresa al login (Requisito 2)

## 5. Control de acceso
- [ ] 5.1 Redirigir al login a quien no tenga sesión iniciada (Requisito 4)
- [ ] 5.2 Negar el acceso a la gestión de usuarios si el rol no es administrador (Requisito 4)

## 6. Gestión de cuentas
- [ ] 6.1 Crear la vista `lista.php` con la tabla de usuarios (Requisito 3)
- [ ] 6.2 Crear la vista `formulario.php` para crear y editar usuarios (Requisito 3)
- [ ] 6.3 Crear `UsuarioController.php` con crear, editar y desactivar, guardando la contraseña con `password_hash()` (Requisito 3)
- [ ] 6.4 Validar correo repetido y contraseña de mínimo 8 caracteres (Requisito 3)

## 7. Cierre del sprint
- [ ] 7.1 Probar manualmente todos los criterios de aceptación de requirements.md
- [ ] 7.2 Actualizar el README con las instrucciones para ejecutar el proyecto