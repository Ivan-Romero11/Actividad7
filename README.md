# Actividad7
# Sistema de Gestión de Citas Médicas

Este proyecto es una aplicación web desarrollada en PHP con un enfoque MVC personalizado (Modelo - Vista - Controlador). Permite gestionar un sistema de citas médicas donde los usuarios pueden registrarse como pacientes o médicos, agendar citas, y administrar información relacionada a especialidades médicas.

##  Objetivo del Proyecto

El objetivo principal es implementar un sistema CRUD funcional utilizando clases personalizadas sin depender de frameworks externos, con una arquitectura organizada y escalable. Este sistema es ideal para clínicas pequeñas o como proyecto académico para aprender PHP orientado a objetos.

---

## Instalación y Ejecución

### Requisitos
- PHP >= 7.4
- Servidor web (Apache, Nginx o XAMPP)
- MySQL o MariaDB
- Navegador web

###  Instrucciones

1. **Clona el repositorio**  
   ```bash
   git clone https://github.com/tuusuario/sistema-citas-medicas.git
   cd sistema-citas-medicas
Crea una base de datos en MySQL:

sql
Copiar
Editar
CREATE DATABASE sistema_citas;
Importa el archivo sistema_reservas_medicas.sql incluido.

Configura el archivo config.php
Edita los datos de conexión a la base de datos:

php
Copiar
Editar
define('DB_HOST', 'localhost');
define('DB_NAME', 'sistema_citas');
define('DB_USER', 'root');
define('DB_PASS', '');
Ejecuta el proyecto

Si usas XAMPP, coloca el proyecto en la carpeta htdocs.

Accede desde el navegador a:

ruby
Copiar
Editar
http://localhost/sistema-citas-medicas/public
📁 Estructura del Proyecto
bash
Copiar
Editar
app/
│
├── Classes/               # Clases de núcleo (Router, View, DB, Autoloader)
│   ├── Router.php
│   ├── View.php
│   └── Db.php
│
├── Controllers/           # Controladores que gestionan la lógica
│   ├── CitaController.php
│   └── UsuarioController.php
│
├── Models/                # Modelos de datos y acceso a BD
│   ├── CitaModel.php
│   ├── MedicoModel.php
│   ├── UsuarioModel.php
│   └── EspecialidadModel.php
│
├── Resources/             # Vistas y recursos organizados
│   ├── Views/
│   │   ├── auth/          # Login y registro
│   │   ├── citas/         # Crear y listar citas
│   │   ├── patient/       # Dashboard para pacientes
│   │   └── error/         # Página de errores
│   └── Layouts/           # Plantillas comunes
│
├── Public/                # Carpeta pública raíz (index.php)
│
├── .htaccess              # Reescritura de URLs amigables
├── config.php             # Configuración general
└── sistema_reservas_medicas.sql # Script para la base de datos
