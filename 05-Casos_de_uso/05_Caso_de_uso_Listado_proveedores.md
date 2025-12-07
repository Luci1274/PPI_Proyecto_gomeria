# Caso de uso: Listado de proveedores
# Actores: Administrador
# Precondiciones: ...
# Caminos Básico:

1. El administrador puede buscar y/o filtrar la lista por nombre, CUIT o estado y navegar entre páginas.
2. El administrador selecciona un proveedor para ver detalles, editar o eliminar.
3. El sistema abre la vista correspondiente (detalle/edición/confirmación de eliminación) o ejecuta la acción solicitada y actualiza la lista.

# Caminos Alternativos:
1.A Búsqueda sin resultados
    1.A.1 El sistema muestra mensaje "No se encontraron proveedores".
    1.A.2 El administrador puede limpiar filtros o crear un nuevo proveedor.

1.B Error al cargar la lista
    1.B.1 El sistema muestra mensaje de fallo y ofrece opción de reintentar.

2.A Edición desde el listado
    2.A.1 El administrador modifica datos y presiona "Guardar".
    2.A.2 El sistema valida y guarda los cambios o muestra errores de validación; luego actualiza la lista.

2.B Eliminación desde el listado
    2.B.1 El administrador confirma eliminación.
    2.B.2 El sistema elimina el proveedor o muestra error si existen restricciones y actualiza la lista.

# Postcondiciones: La lista se muestra correctamente; si se editaron o eliminaron proveedores, la lista refleja los cambios.
# Escenarios de Éxito:
1. El administrador visualiza, filtra y navega la lista de proveedores correctamente.
2. Las operaciones de ver, editar o eliminar se completan y la lista muestra un mensaje de confirmación.

# Escenarios de Fracaso:
1. No hay proveedores que coincidan con los criterios de búsqueda.
2. Error de conexión a la base de datos al cargar o actualizar la lista; el sistema muestra un mensaje de fallo.
3. Error de validación al editar o restricción al eliminar; la operación no se completa y se informa al administrador.