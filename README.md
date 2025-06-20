# Plantilla Odoo + Postgres con Docker Compose

Esta plantilla te permite desplegar fácilmente **Odoo Version Community**, un sistema ERP (Enterprise Resource Planning) de código abierto, ideal para gestionar ventas, inventario, contabilidad, recursos humanos y mucho más. Puedes usar esta automatización para pruebas, desarrollo de módulos personalizados o como base para proyectos empresariales.

## ¿Qué es Odoo?

Odoo es una plataforma modular que integra aplicaciones de gestión empresarial en un solo lugar. Es ampliamente utilizada por empresas de todos los tamaños para digitalizar y automatizar procesos.

## ¿Qué incluye este repositorio?

- **Odoo**: Instalado y listo para usar.
- **PostgreSQL**: Base de datos persistente.
- **Soporte para módulos personalizados**: Solo agrega tus módulos en la carpeta `addons`.
- **Automatización con Docker Compose**: Despliegue rápido y sencillo.

## ¿Cómo probar y ejecutar esta plantilla?

1. **Clona este repositorio**
   ```bash
   git clone <URL-de-este-repositorio>
   cd odoo
   ```

2. **Revisa o edita el archivo `.env`** con las variables necesarias:
   ```env
   POSTGRES_USER=odoo
   POSTGRES_PASSWORD=odoo
   POSTGRES_DB=postgres
   ```

3. Crea carpeta `addons` en la raiz para los modulos personalizados

4. Crear carpeta `postgresql` en la raiz para persistir datos

3. **Levanta los servicios**
   ```bash
   docker-compose up -d
   ```

4. **Accede a Odoo**
   Abre tu navegador y entra a: [http://localhost:8069](http://localhost:8069)

5. **¡A disfrutar!**
   Crea tu base de datos, explora los módulos de Odoo y comienza a gestionar tu empresa o proyecto.

## Personalización

- Modifica `odoo.conf` para cambiar la configuración de Odoo (usuario, contraseña, rutas de addons, etc.).
- Agrega tus módulos personalizados en la carpeta `addons`.
- Los datos de la base de datos se almacenan en la carpeta `postgresql/` para persistencia.

## Requisitos

- Docker
- Docker Compose

## Notas

- Para detener los servicios:
  ```bash
  docker-compose down
  ```
- Para ver los logs:
  ```bash
  docker-compose logs -f
  ```
- Si cambias credenciales, actualiza tanto `.env` como `odoo.conf` para mantener la coherencia.

---

¡Listo! Así puedes probar, personalizar y disfrutar de Odoo en