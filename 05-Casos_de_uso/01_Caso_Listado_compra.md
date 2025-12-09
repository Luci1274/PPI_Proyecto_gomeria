# Caso de uso: Listado de Compras
# Actores: Administrador
# Precondiciones: ...

# Caminos Básico:
1. El administrador puede buscar y/o filtrar la lista por nombre del proveedor, estado de la compra y navegar entre páginas.
2. El sistema muestra la lista de compras según los criterios seleccionados.
3. El administrador selecciona una compra para ver detalles o eliminar.
4. El sistema abre la vista correspondiente (detalle/confirmación de dar de baja) o ejecuta la acción solicitada y actualiza la lista.

# Caminos Alternativos:
1.A Búsqueda sin resultados
    1.A.1 El sistema muestra mensaje "No se encontraron compras".
    1.A.2 El administrador puede limpiar filtros o iniciar una nueva compra.

1.B Error al cargar la lista
    1.B.1 El sistema muestra mensaje de fallo y ofrece opción de reintentar.

3.A dar de baja desde el listado
    3.A.1 El administrador confirma dar de baja.

# Postcondiciones: La lista se muestra correctamente; si se eliminaron compras, la lista refleja los cambios.
# Escenarios de Éxito:
1. El administrador visualiza, filtra y navega la lista de compras correctamente.
2. La operación de eliminar se completa y la lista muestra un mensaje de confirmación.

# Escenarios de Fracaso:
1. No hay compras que coincidan con los criterios de búsqueda.
2. Error de conexión a la base de datos al cargar o actualizar la lista; el sistema muestra un mensaje de fallo.