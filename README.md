# 🧾 FerreFactura — Backend

API REST para un sistema de gestión comercial: **productos, facturas, inventario, usuarios, caja diaria, deudores y reportes**.

> Proyecto de portafolio. Para un entorno real, revisa primero la configuración de seguridad, credenciales, permisos y despliegue.

## Tecnologías

- Python y **Django 5**
- **Django REST Framework** y autenticación por tokens/JWT
- **SQL Server** mediante `mssql-django` / `pyodbc`
- Documentación de API con **Swagger** y **ReDoc**

## Funcionalidades presentes en el código

| Módulo | Alcance |
| --- | --- |
| Usuarios | Gestión y control de acceso |
| Productos | Catálogo, precios y existencias |
| Facturación | Facturas, detalles, descuentos y ventas |
| Caja diaria | Registro y consulta de operaciones |
| Deudores | Registro de deudas y pagos |
| Reportes | Estadísticas, ventas diarias/anuales y ganancias por producto |

## Estructura

```text
FerreFac/        # Configuración de Django
facturacion/     # Modelos, serializadores, vistas, rutas y lógica
manage.py        # Herramienta de administración
requirements.txt # Dependencias de Python
```

## Ejecución local (orientativa)

1. Instala Python y los controladores ODBC necesarios para tu versión de SQL Server.
2. Crea y activa un entorno virtual de Python fuera del repositorio.
3. Instala las dependencias:
   ```bash
   pip install -r requirements.txt
   ```
4. **Configura primero la conexión de base de datos y las variables de seguridad** según tu entorno local. No publiques contraseñas ni claves.
5. Ejecuta las migraciones y el servidor:
   ```bash
   python manage.py migrate
   python manage.py runserver
   ```

La disponibilidad de la API depende de que se configure correctamente la base de datos y el entorno.

## Rutas relevantes

- `/api/` — recursos de negocio
- `/admin/` — administración de Django
- `/swagger/` — explorador de la API
- `/redoc/` — documentación de la API

## Frontend

La interfaz está en [ferrefactura-frontend](https://github.com/daniel102sa1/ferrefactura-frontend).

## Calidad y mejoras pendientes

- Revisar la configuración de secretos y accesos a la base de datos.
- Añadir instrucciones reproducibles de entorno y datos de ejemplo.
- Fortalecer pruebas automatizadas, validaciones y documentación de despliegue.

**Autor:** [Jeancarlo Daniel Rodríguez Pivaral](https://github.com/daniel102sa1)
