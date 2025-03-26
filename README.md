# GESTOR DE PRODUCTOS CON TKINTER Y SQLITE
===========================================

## Descripción General

Esta aplicación de escritorio permite gestionar un inventario de productos de manera sencilla y eficiente. Desarrollada con Python, Tkinter para la interfaz gráfica y SQLite para el almacenamiento de datos, ofrece todas las funcionalidades básicas de un sistema CRUD (Crear, Leer, Actualizar, Eliminar).

## Requisitos

- Python 3.6 o superior
- Bibliotecas requeridas (incluidas en Python estándar):
  - tkinter
  - sqlite3

## Estructura de Archivos

- `app.py`: Script principal que contiene toda la lógica de la aplicación.
- `database/productos.db`: Base de datos SQLite donde se almacenan los productos.
- `recursos/M6_P2_icon.ico`: Icono de la aplicación.

## Funcionalidades Principales

1. **Registro de Productos**:
   - Formulario para ingresar nombre y precio de nuevos productos.
   - Validación de datos para asegurar entradas correctas.
   - Mensajes de confirmación tras operaciones exitosas.

2. **Visualización de Productos**:
   - Tabla que muestra todos los productos registrados.
   - Ordenamiento automático por nombre en orden descendente.

3. **Edición de Productos**:
   - Ventana emergente para modificar productos existentes.
   - Opción de cambiar nombre y/o precio.
   - Actualización automática de la tabla tras ediciones.

4. **Eliminación de Productos**:
   - Eliminación directa seleccionando un producto de la tabla.
   - Confirmación visual de la eliminación.

## Instrucciones de Uso

### Iniciar la Aplicación

1. Ejecute el archivo `app.py` con Python:

2. La aplicación se abrirá mostrando la ventana principal con el formulario de registro y la tabla de productos.

### Registrar un Nuevo Producto

1. En el formulario "Registrar un nuevo Producto":
- Ingrese el nombre del producto en el campo "Nombre".
- Ingrese el precio del producto en el campo "Precio" (debe ser un número válido mayor que 0).
- Haga clic en el botón "Guardar Producto".

2. Si la operación es exitosa:
- Se mostrará un mensaje de confirmación.
- El formulario se limpiará automáticamente.
- El nuevo producto aparecerá en la tabla.

### Editar un Producto

1. En la tabla de productos:
- Seleccione el producto que desea editar haciendo clic sobre él.
- Haga clic en el botón "EDITAR" ubicado debajo de la tabla.

2. En la ventana emergente "Editar Producto":
- Verá los datos actuales del producto (nombre y precio).
- Ingrese el nuevo nombre y/o precio en los campos correspondientes.
- Si deja un campo vacío, se mantendrá el valor original.
- Haga clic en "Actualizar Producto" para confirmar los cambios.

3. Si la operación es exitosa:
- La ventana de edición se cerrará automáticamente.
- Se mostrará un mensaje de confirmación.
- La tabla se actualizará con los nuevos datos.

### Eliminar un Producto

1. En la tabla de productos:
- Seleccione el producto que desea eliminar haciendo clic sobre él.
- Haga clic en el botón "ELIMINAR" ubicado debajo de la tabla.

2. Si la operación es exitosa:
- Se mostrará un mensaje de confirmación.
- El producto desaparecerá de la tabla.

## Estructura de la Base de Datos

La aplicación utiliza una base de datos SQLite con una única tabla:

**Tabla: producto**
- `id` (INTEGER): Identificador único, clave primaria, autoincremental.
- `nombre` (TEXT): Nombre del producto, no puede ser nulo.
- `precio` (REAL): Precio del producto, no puede ser nulo.

## Detalles Técnicos

### Interfaz Gráfica

La interfaz está construida con Tkinter y organizada en una estructura de grid (cuadrícula):
- Formulario de registro en la parte superior.
- Tabla de productos en el centro.
- Botones de acción en la parte inferior.

### Estilos y Personalización

- Fuentes personalizadas para mejorar la legibilidad.
- Estilos específicos para la tabla (Treeview).
- Botones con estilos ttk para una apariencia moderna.

### Manejo de Errores

La aplicación incluye validaciones para:
- Campos obligatorios (nombre y precio).
- Formato correcto para el precio (número válido mayor que 0).
- Selección de producto antes de editar o eliminar.

## Solución de Problemas

1. **Error al iniciar la aplicación**:
- Verifique que Python 3.6+ esté instalado correctamente.
- Asegúrese de que las bibliotecas tkinter y sqlite3 estén disponibles.

2. **Error al guardar productos**:
- Compruebe los permisos de escritura en la carpeta 'database'.
- Verifique que el formato del precio sea correcto (número válido).

3. **La tabla no muestra productos**:
- Verifique que la base de datos exista y contenga la tabla 'producto'.
- Compruebe la conexión a la base de datos.

4. **Errores en la edición de productos**:
- Asegúrese de seleccionar un producto antes de hacer clic en "EDITAR".
- Verifique que los nuevos valores cumplan con las validaciones.
