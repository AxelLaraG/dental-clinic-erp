# DentalCare - Clinic Management ERP

Sistema integral de planificación de recursos empresariales (ERP) desarrollado en Python para la administración de clínicas odontológicas. La aplicación de escritorio proporciona herramientas centralizadas para la gestión de pacientes, control de expedientes médicos, programación de citas y control de accesos basado en roles.

## Módulos y Características

El sistema está construido bajo una arquitectura modular, dividiendo las responsabilidades del negocio en componentes aislados:

* **Gestión de Identidad y Accesos (IAM):** Autenticación segura y menús dinámicos dependientes del rol del usuario (Administrador vs. Dentista) (`MenuPrincipal.py`, `MenuPrincipalDentista.py`).
* **Control de Expedientes Médicos (EHR):** Operaciones CRUD completas para la creación y actualización del historial clínico de los pacientes (`CrudExpediente.py`).
* **Motor de Agendamiento:** Interfaz gráfica dedicada para la programación, consulta y administración de citas médicas (`CitasWindow.py`).
* **Administración de Personal y Usuarios:** Módulos de control interno para el registro y gestión de especialistas y personal administrativo (`CrudDentista.py`, `CrudUser.py`).

## Stack Tecnológico

* **Lenguaje:** Python 3.x
* **Interfaz Gráfica (GUI):** Integración de archivos `.ui` (diseñados visualmente) acoplados a controladores lógicos en Python.
* **Base de Datos:** Motor SQL relacional con esquemas estructurados para mantener la integridad referencial de la clínica.

## 📦 Instalación y Configuración del Entorno

1. **Clonar el repositorio:**
   ```bash
   git clone https://github.com/AxelLaraG/dental-clinic-erp.git
   cd dental-clinic-erp
   ```
2. Despliegue de Base de Datos:
   Antes de ejecutar la aplicación, inicializa la base de datos ejecutando los scripts SQL ubicados en DentalCare/Clinica_DataBase/ y DentalCare/Expedientes/ en tu motor de base de datos local. Asegúrate de configurar las credenciales de conexión en tu entorno.
3. Ejecución:
   El punto de entrada principal del sistema inicia el proceso de autenticación. Ejecuta:
      ```
      python DentalCare/Login/LoginWindow.py
      ```
## Arquitectura de la Interfaz
El proyecto sigue un patrón de separación entre el diseño visual y la lógica de negocio. Las interfaces fueron diseñadas visualmente y se almacenan como archivos `.ui` (XML nativo) en sus respectivos directorios modulares. Los scripts de Python asociados cargan estas vistas y manejan los eventos, señales y transacciones hacia la base de datos de manera limpia.
