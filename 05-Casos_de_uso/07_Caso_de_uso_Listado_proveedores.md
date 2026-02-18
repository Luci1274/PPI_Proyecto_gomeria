# Caso de uso: Listado de proveedores
# Actores: Administrador
# Precondiciones: ...
# Caminos Básico:

1. El Administrador ingresa criterios de búsqueda y/o filtrado.
2. El sistema obtiene los proveedores según los criterios ingresados.
3. El sistema muestra la lista paginada de proveedores.
4. El Administrador selecciona un proveedor de la lista.


# Caminos Alternativos:
1.A Búsqueda sin resultados
    1.A.1 El sistema muestra mensaje "No se encontraron proveedores".
    1.A.2 El administrador puede limpiar filtros o crear un nuevo proveedor.

1.B Error al cargar la lista
    1.B.1 El sistema muestra mensaje de fallo y ofrece opción de reintentar.

# Postcondiciones: La lista se muestra correctamente
# Escenarios de Éxito:
1. El administrador visualiza, filtra y navega la lista de proveedores correctamente.


# Escenarios de Fracaso:
1. No hay proveedores que coincidan con los criterios de búsqueda.
2. Error de conexión a la base de datos al cargar o actualizar la lista; el sistema muestra un mensaje de fallo.