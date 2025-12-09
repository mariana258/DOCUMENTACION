1. Información General

Nombre del sistema: ECOSOFT
Tipo de sistema: Aplicación web
Arquitectura: Cliente – Servidor
Lenguajes de programación: Python (Backend) y /React (Frontend)

2. Arquitectura Técnica

El sistema ECOSOFT está compuesto por los siguientes componentes:

Frontend: React.js

Backend: FastAPI (Python)

Base de datos: MySQL

Servidor de desarrollo: Uvicorn

Diagrama de Arquitectura
[ Navegador Web ]
        |
[ Frontend - React.js ]
        |
[ Backend - FastAPI ]
        |
[ Base de Datos - MySQL ]

3. Estructura del Proyecto
3.1 Estructura del Backend
backend/
│── main.py
│── database.py
│── models/
│   ├── usuario.py
│   ├── material.py
│   └── pedido.py
│── schemas/
│── routes/
│   ├── auth.py
│   ├── usuarios.py
│   ├── materiales.py
│   └── pedidos.py


Descripción:

main.py: Punto de entrada de la aplicación.

database.py: Configuración de la conexión a la base de datos.

models/: Definición de los modelos de la base de datos.

schemas/: Esquemas de validación con Pydantic.

routes/: Definición de las rutas (endpoints) del sistema.

3.2 Estructura del Frontend
frontend/
│── src/
│   ├── pages/
│   ├── components/
│   ├── config/
│   └── App.jsx


Descripción:

pages/: Vistas principales del sistema.

components/: Componentes reutilizables de la interfaz.

config/: Servicios de la API.

App.jsx: Componente principal de la aplicación.

4. Configuración del Entorno
4.1 Variables de Entorno

Archivo README.md o .env (backend):

DATABASE_URL=mysql+pymysql://user:password@localhost/ecosoft
SECRET_KEY=clave_super_secreta
ALGORITHM=HS256
ACCESS_TOKEN_EXPIRE_MINUTES=30


Descripción de variables:

DATABASE_URL: Cadena de conexión a la base de datos.

SECRET_KEY: Clave para generación de tokens JWT.

ALGORITHM: Algoritmo de encriptación.

ACCESS_TOKEN_EXPIRE_MINUTES: Tiempo de expiración del token.

5. Instalación Técnica
5.1 Instalación del Backend
python -m venv venv
venv\Scripts\activate
pip install -r requirements.txt
uvicorn main:app --reload

5.2 Instalación del Frontend
npm install
npm run dev

6. Endpoints Principales (API)
6.1 Módulo de Usuarios
Método	Endpoint	Descripción
POST	/auth/login	Iniciar sesión
GET	/usuarios	Listar usuarios
POST	/usuarios	Crear usuario
6.2 Módulo de Materiales
Método	Endpoint	Descripción
GET	/materiales	Listar materiales
POST	/materiales	Crear material
PUT	/materiales/{id}	Actualizar material
DELETE	/materiales/{id}	Eliminar material
6.3 Módulo de Pedidos
Método	Endpoint	Descripción
GET	/pedidos	Listar pedidos
POST	/pedidos	Crear pedido
PUT	/pedidos/{id}/estado	Cambiar estado del pedido
7. Seguridad del Sistema

El sistema implementa las siguientes medidas de seguridad:

Autenticación basada en JWT (JSON Web Token).

Encriptación de contraseñas mediante bcrypt.

Validación de datos de entrada con Pydantic.

8. Mantenimiento Técnico

Para mantener el sistema en óptimas condiciones:

Realizar respaldos periódicos de la base de datos.

Mantener actualizadas las dependencias del proyecto.

Monitorear los logs del servidor para detectar errores.

9. Requisitos Técnicos para el Usuario Final

Para utilizar el sistema, el usuario final debe:

Tener acceso a internet.

Utilizar un navegador actualizado (Chrome, Edge o Firefox).

Contar con credenciales de usuario válidas.

10. Flujo de Uso del Sistema (Vista Técnica–Funcional)
10.1 Inicio de Sesión (Flujo)

El frontend envía credenciales al endpoint /auth/login.

El backend valida los datos.

Se genera un token JWT.

El usuario accede al Dashboard.

10.2 Panel Principal (Dashboard)

Desde el panel principal, el sistema habilita:

Consulta de pedidos.

Acceso a módulos de materiales.

Administración de perfil.

10.3 Gestión de Materiales (Flujo Técnico)

Agregar material:

El frontend envía una petición POST /materiales.

El backend valida datos con Pydantic.

Se guarda en la base de datos.

Editar material:

Se envía PUT /materiales/{id}.

Se actualiza el registro en MySQL.

Eliminar material:

Se envía DELETE /materiales/{id}.

Se elimina el registro.

10.4 Gestión de Pedidos (Flujo Técnico)

Crear pedido:

POST /pedidos

Se guarda en la base de datos.

Cambiar estado:

PUT /pedidos/{id}/estado

Se actualiza el estado del pedido.

11. Roles de Usuario
Rol	Permisos principales
Administrador	Control total del sistema
Empleado	Gestión de pedidos y visualización de stock
Supervisor	Generación de reportes
12. Preguntas Frecuentes Técnicas (FAQ)

¿Qué hacer si falla la conexión a la base de datos?
Verificar el valor de DATABASE_URL y el estado del servidor MySQL.

¿Qué hacer si el sistema no inicia?
Revisar los logs de Uvicorn y reinstalar dependencias.

13. Soporte Técnico

Para soporte técnico:

Contactar al administrador del sistema.

Revisar los logs del sistema.

14. Glosario Técnico

Inventario: Control de existencias de materiales.

Pedido: Registro de solicitud de materiales.

JWT: Mecanismo de autenticación por token.

Pydantic: Librería usada para validar datos.
