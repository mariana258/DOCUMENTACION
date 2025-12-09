📘 Documentación del Proyecto ECOSOFT 


ECOSOFT es una aplicación web desarrollada para la gestión de inventarios, pedidos, materiales y usuarios en una empresa. El sistema permite automatizar procesos de control de stock, realizar pedidos y administración de usuarios con diferentes roles.

l.

Objetivo General

Desarrollar una aplicación de software para tener un control de los procesos

logísticos de una empresa de reciclaje, desde la recepción de materiales hasta la entrega de sus productos.


Objetivos Específicos

•	Recolectar la información sobre el proceso de los materiales.

•	Diseñar una interfaz intuitiva

•	Implementar un sistema de registro digital para clientes, empleados y proveedores que centralice la información de manera segura.

•	Automatizar el agendamiento y la gestión de pedidos para optimizar los tiempos de atención y recolección de materiales.

•	Generar reportes automáticos de facturación, inventario y logística que faciliten la toma de decisiones estratégicas.

•	Optimizar el registro y control del inventario de materiales reciclados, garantizando trazabilidad en su transformación.

•	Promover la innovación en la industria del reciclaje mediante la digitalización de procesos tradicionalmente manuales y desorganizados.


4. Tecnologías Utilizadas
5. 
Para el desarrollo del proyecto de reciclaje se eligió el stack React + API REST con 
Python (FastAPI) + MySQL porque ofrece un equilibrio entre simplicidad, velocidad 
de desarrollo y facilidad de mantenimiento.
React permite construir interfaces modernas, rápidas y fáciles de usar. Su enfoque en 
componentes facilita el diseño de pantallas reutilizables para clientes, proveedores, 
administradores y domiciliarios.
El uso de API REST con Python (FastAPI ) simplifica la comunicación entre el 
frontend y la base de datos. Python es un lenguaje muy accesible y cuenta con una gran 
comunidad, lo que facilita encontrar soluciones y mantener el proyecto a largo plazo.
La base de datos MySQL fue elegida por su confiabilidad y porque se adapta bien al 
tipo de datos estructurados que maneja el sistema, como pedidos, usuarios, rutas y 
pagos. Además, su integración con Python es sencilla y eficiente.
Este stack resulta adecuado para un proyecto que necesita desarrollarse de forma ágil, 
con un equipo pequeño y recursos limitados. También permite crecer y adaptarse a 
futuras necesidades, sin que la complejidad tecnológica sea una barrera

4.3 Control de Versiones

Git

GitHub

5. Arquitectura del Sistema

El sistema se basa en una arquitectura cliente-servidor:

El frontend se comunica con el backend mediante peticiones HTTP (API REST).

El backend procesa las solicitudes y se comunica con la base de datos.

La base de datos almacena toda la información del sistema.

[ Usuario ]
     ↓
[ Frontend - React ]
     ↓  HTTP/JSON
[ Backend - FastAPI ]
     ↓
[ Base de Datos - MySQL ]

6. Requisitos Funcionales
 <img width="476" height="578" alt="image" src="https://github.com/user-attachments/assets/14c20c8a-014d-40ed-9be0-5bc0069a8287" />
 <img width="476" height="578" alt="image" src="https://github.com/user-attachments/assets/7d6eb55f-bb07-4e42-bba8-cca025b902a1" />
 <img width="476" height="578" alt="image" src="https://github.com/user-attachments/assets/a0fa2a10-530d-4240-a82a-7778ffb7b7d0" />
 <img width="476" height="578" alt="image" src="https://github.com/user-attachments/assets/7c63b795-4620-4a22-b814-11ae859b89aa" />
 
6.2 Requisitos No Funcionales
<img width="476" height="578" alt="image" src="https://github.com/user-attachments/assets/e0469133-e3a9-4cdf-8d35-fd103d2ff424" />
<img width="476" height="578" alt="image" src="https://github.com/user-attachments/assets/26634673-0617-474e-b209-43a39714c3f5" />
<img width="476" height="578" alt="image" src="https://github.com/user-attachments/assets/32dcf147-0f1b-489c-98b1-6811e3e84252" />
<img width="476" height="578" alt="image" src="https://github.com/user-attachments/assets/e1510b18-06ff-4d43-8b26-059683443c0f" />
<img width="476" height="578" alt="image" src="https://github.com/user-attachments/assets/fe0a3b2d-5ead-44a9-a8cc-683f25f934a8" />


7. Modelo de Base de Datos
<img width="476" height="578" alt="image" src="https://github.com/user-attachments/assets/72a3a25a-3c27-4e60-9780-a83cfe1aba06" />


8. Instalación del Proyecto
1. Instalar dependencias
```powershell
cd "C:\Users\almengol\OneDrive\Desktop\ecosoft\backend"
python -m pip install -r requirements.txt
python -m pip install -r "..\requirements-dev.txt"
```

2. Crear la base de datos (opcional, recommended to fully run the app)
 - Ejecuta el archivo `ecosoft.sql` en tu servidor MySQL (por ejemplo con MySQL Workbench o `mysql` CLI).

3. Variables de entorno
 - Crea un `.env` en `backend/` con las variables: MYSQL_USER, MYSQL_PASSWORD, MYSQL_HOST, MYSQL_DB, MYSQL_PORT, SECRET_KEY, etc.

4. Ejecutar la aplicación
```powershell
cd "C:\Users\almengol\OneDrive\Desktop\ecosoft\backend"
python -m uvicorn main:app --reload --host 127.0.0.1 --port 8000
```
8.1 Requisitos Previos

Python 3.10+

Node.js 18+

MySQL Server

Git

8.2 Instalación Backend
git clone https://github.com/mariana258/ECOSOFT.git
cd ECOSOFT/backend
python -m venv venv
venv\Scripts\activate
pip install -r requirements.txt
uvicorn main:app --reload

8.3 Instalación Frontend
cd ../frontend
npm install
npm run dev

9. Manual de Usuario
 primera pagina(introduccion sobre el proyecto)
   <img width="476" height="578" alt="image" src="https://github.com/user-attachments/assets/a4b58fd2-f67e-4b70-80b5-354b0697b82f" />

9.1 Registro
<img width="476" height="578" alt="image" src="https://github.com/user-attachments/assets/f58ef389-238f-446a-b7ff-da94b5d53910" />

Inicio de Sesión
<img width="476" height="578" alt="image" src="https://github.com/user-attachments/assets/801c4191-a9b9-4196-affc-e893f3d28f29" />
Ingresar al sistema.

Escribir correo y contraseña.

Presionar “Ingresar”.

9.2 Realizar pedidos

<img width="476" height="578" alt="image" src="https://github.com/user-attachments/assets/8cff059c-49e2-451e-8466-1ad37a5bfefd" />

Crear pedidos.
completar los campos.
verificar informacion y comprobante de pedido.

9.3 Descargar comprobante
<img width="1257" height="216" alt="image" src="https://github.com/user-attachments/assets/27d8b78e-b7b0-4a68-9a93-b694b06d220c" />

Despues de realizar su pedido, aparece informacion especifica de la compra.
Dar click en descargar.


9.4 Enviar quejas o reclamos

<img width="476" height="578" alt="image" src="https://github.com/user-attachments/assets/439270cf-bcb4-405d-a804-7486b9a7d691" />
colocar el motivo de la queja.
dar click a enviar.




🛠️ MANUAL TÉCNICO
Proyecto: ECOSOFT 
1. Información General

Nombre del sistema: ECOSOFT
Tipo: Aplicación web
Arquitectura: Cliente – Servidor
Lenguajes: Python y react

2. Arquitectura Técnica

El sistema está compuesto por:

Frontend: React.js

Backend: FastAPI (Python)

Base de Datos: MySQL

Servidor de desarrollo: Uvicorn

Diagrama:

[ Navegador ]
      |
[ React Frontend ]
      |
[ FastAPI Backend ]
      |
[ MySQL Database ]

3. Estructura del Proyecto
3.1 Backend
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

3.2 Frontend
frontend/
│── src/
│   ├── pages/
│   ├── components/
│   ├── services/
│   └── App.jsx

4. Configuración del Entorno
4.1 Variables de Entorno

Archivo readme.md(backend):

DATABASE_URL=mysql+pymysql://user:password@localhost/ecosoft
SECRET_KEY=clave_super_secreta
ALGORITHM=HS256
ACCESS_TOKEN_EXPIRE_MINUTES=30

5. Instalación Técnica
5.1 Backend
python -m venv venv
venv\Scripts\activate
pip install -r requirements.txt
uvicorn main:app --reload

5.2 Frontend
npm install
npm run dev

6. Endpoints Principales (API)
Usuarios
Método	Endpoint	Descripción
POST	/auth/login	Iniciar sesión
GET	/usuarios	Listar usuarios
POST	/usuarios	Crear usuario
Materiales
Método	Endpoint	Descripción
GET	/materiales	Listar materiales
POST	/materiales	Crear material
PUT	/materiales/{id}	Actualizar material
DELETE	/materiales/{id}	Eliminar material
Pedidos
Método	Endpoint	Descripción
GET	/pedidos	Listar pedidos
POST	/pedidos	Crear pedido
PUT	/pedidos/{id}/estado	Cambiar estado
7. Seguridad

Autenticación basada en JWT

Contraseñas encriptadas con bcrypt

Validaciones de datos mediante Pydantic

8. Mantenimiento Técnico

Respaldos periódicos de la base de datos.

Actualización de dependencias.

Monitoreo de logs del servidor.


2. Requisitos para el Usuario

Tener acceso a internet.

Usar un navegador actualizado (Chrome, Edge o Firefox).

Tener credenciales de usuario.

3. Guía de Uso Paso a Paso
3.1 Iniciar Sesión

Abrir el sistema.

Escribir correo electrónico.

Escribir contraseña.

Hacer clic en Iniciar sesión.

3.2 Panel Principal (Dashboard)

Desde el panel principal el usuario puede:

Ver resumen de sus pedidos

Acceder a materiales

Acceder a pedidos

Administrar su perfil

3.3 Gestión de Materiales

Para agregar un material:

Ir al menú Materiales.

Clic en Nuevo material.

Llenar el formulario (nombre, descripción, precio, stock).

Clic en Guardar.

Para editar un material:

Seleccionar el material.

Clic en Editar.

Modificar los datos.

Clic en Actualizar.

Para eliminar un material:

Seleccionar el material.

Clic en Eliminar.

Confirmar.

3.4 Gestión de Pedidos

Para crear un pedido:

Ir a Pedidos.

Clic en Nuevo pedido.

Seleccionar los materiales.

Guardar.

Para cambiar el estado del pedido:

Seleccionar el pedido.

Elegir el estado:

Pendiente

En proceso

Completado

4. Roles de Usuario

Administrador: control total del sistema.

Empleado: puede gestionar pedidos y ver inventario.

Supervisor: puede generar reportes.

5. Preguntas Frecuentes (FAQ)

¿Qué hago si olvido mi contraseña?
Contactar al administrador del sistema.

¿Por qué no puedo eliminar un registro?
Puede ser por permisos de tu rol.

6. Soporte Técnico

En caso de fallos o dudas, comunicarse con el administrador del sistema.

7. Glosario

Inventario: Control de existencia de materiales.

Pedido: Solicitud de materiales.

Usuario: Persona registrada en el sistema.

