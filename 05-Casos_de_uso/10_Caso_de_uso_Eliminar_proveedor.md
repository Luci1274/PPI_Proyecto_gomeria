# Caso de uso: Eliminar proveedor
# Actores: Administrador
# Precondiciones: Caso de uso 05 Listado de proveedores. El proveedor existe y está seleccionado desde el listado.
# Caminos Básico:

1. El administrador selecciona un proveedor en el listado y elige "Eliminar proveedor".
2. El sistema solicita confirmación de eliminación (modal/diálogo).
3. El administrador confirma la eliminación.
4. El sistema elimina el proveedor de la base de datos (o marca como inactivo según políticas) y actualiza el listado.
5. El sistema regresa al caso de uso 05 mostrando la lista actualizada y un mensaje de confirmación.

# Caminos Alternativos:
1.A Eliminación cancelada.
    
    1.A.1 El administrador cancela en el diálogo; el sistema regresa al caso de uso 05 sin cambios.

1.B Restricción por integridad referencial (existen registros relacionados).
    
    1.B.1 El sistema informa que no se puede eliminar por dependencias y ofrece alternativas (marcar como inactivo, ver dependencias).
    1.B.2 El administrador decide la acción a seguir (cancelar, inactivar, gestionar dependencias).

1.C Error al eliminar por fallo en base de datos.
    
    1.C.1 El sistema muestra mensaje de error y ofrece reintentar.

# Postcondiciones: proveedor eliminado o marcado como inactivo en la base de datos; la lista refleja el cambio.
# Escenarios de Éxito:
1. El administrador confirma la eliminación y el sistema la realiza, mostrando confirmación.
# Escenarios de Fracaso:
1. Eliminación rechazada por dependencias en la base de datos; no se elimina el proveedor.
2. Error de conexión o fallo en la BD al borrar; la operación no se completa y se informa al administrador.
3. El administrador cancela la operación y no se realizan cambios.