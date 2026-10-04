# Requisitos del Sprint 1: login y cuentas de usuario

## Roles
- Administrador: gestiona las cuentas de usuario
- Cajero: usa el sistema para registrar ventas

## Requisito 1: Inicio de sesión
**Historia:** Como usuario quiero iniciar sesión con mi correo y contraseña para acceder al sistema.

requisitos EARS:

1. [Event-driven] 
Cuando el usuario ingresa correo y contraseña correctos, el sistema debe conceder acceso.

2. [Event-driven]  
Cuando el usuario introduce datos incorrectos, el sistema debe mostrar el mensaje "Correo o contraseña incorrectos", sin indicar cuál falló.

3. [Event-driven]  
Cuando algún campo está vacío, el sistema debe marcarlo en rojo y no enviar el formulario.

4. [State-driven]  
Mientras la cuenta esté desactivada, el sistema debe impedir el acceso.

5. [Event-driven]
Cuando una persona sin sesión acceda a la ruta principal del sistema, el sistema debe mostrar la pantalla de inicio de sesión.

## Requisito 2: Cierre de sesión
**Historia:** Como usuario quiero cerrar sesión para proteger mi cuenta.

Criterios de aceptación:
1. Cuando el usuario cierra sesión, el sistema termina su sesión y lo regresa al login.
2. Después de cerrar sesión, el usuario no puede volver a las páginas internas con el botón "atrás".

## Requisito 3: Gestión de cuentas
**Historia:** Como administrador quiero crear, editar y desactivar cuentas para controlar quién usa el sistema.

Criterios de aceptación:
1. Cuando el administrador crea un usuario, el sistema pide nombre, correo, rol y contraseña.
2. Cuando el correo ya existe, el sistema rechaza el registro y muestra un mensaje.
3. Cuando la contraseña tiene menos de 8 caracteres, el sistema no la acepta.
4. Cuando el administrador desactiva una cuenta, el usuario ya no puede iniciar sesión, pero sus datos se conservan.
5. Las contraseñas se guardan cifradas, nunca en texto plano.

## Requisito 4: Acceso según el rol
**Historia:** Como administrador quiero que cada usuario vea solo lo que le corresponde.

Criterios de aceptación:
1. Cuando un cajero intenta entrar a la gestión de usuarios, el sistema le niega el acceso.
2. Cuando alguien sin sesión intenta entrar a una página interna, el sistema lo envía al login.