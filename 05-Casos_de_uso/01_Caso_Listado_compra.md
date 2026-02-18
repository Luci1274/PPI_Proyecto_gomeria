# Caso de uso: Listado de Compras
# Actores: Administrador
# Precondiciones: ...

# Caminos Básico:
1. El Administrador ingresa criterios de búsqueda y/o filtrado.
2. El sistema obtiene las compras según los criterios ingresados.
3. El sistema muestra la lista paginada de compras.
4. El Administrador selecciona una compra de la lista.
5. El sistema muestra los detalles de la compra seleccionada.

# Caminos Alternativos:
1.A Búsqueda sin resultados
    1.A.1 El sistema muestra mensaje: "No se encontraron compras".
    1.A.2 El administrador puede limpiar filtros o iniciar el registro de una nueva compra.

1.B Error al cargar la lista
    1.B.1 El sistema muestra un mensaje de error indicando que no fue posible cargar los datos.
    1.B.2 El sistema ofrece la opción de reintentar la operación.

3.A dar de baja desde el listado
    3.A.1 El administrador selecciona “Dar de baja”.
    3.A.2 El sistema solicita confirmación.
    3.A.3 El administrador confirma.
    3.A.4 El sistema registra la baja y actualiza la lista.

# Postcondiciones: La lista se muestra correctamente; si se eliminaron compras, la lista refleja los cambios.

# Escenarios de Éxito:
1. El administrador visualiza, filtra y navega la lista de compras sin inconvenientes.
2. La baja de una compra se realiza correctamente y se muestra un mensaje de confirmación.

# Escenarios de Fracaso:
1. No existen compras que coincidan con los criterios ingresados.
2. Ocurre un error al cargar o actualizar la lista (problemas de conexión o base de datos).
3. El sistema muestra el mensaje de fallo correspondiente.