# Caso de uso: Eliminar proveedor
# Actores: Administrador
# Precondiciones: El proveedor existe
# Caminos Básico:

1. El Administrador solicita eliminar un proveedor.
2. El sistema solicita confirmación de la operación.
3. El Administrador confirma.
4. El sistema cambia el estado del proveedor a Inactivo.


# Caminos Alternativos:
1.A El Administrador cancela la operación en la confirmación.
    1.A.1 El sistema cancela la eliminación y mantiene el proveedor activo.

1.B Restricción por integridad referencial (existen registros relacionados).
    
    1.B.1 El sistema informa que no se puede eliminar por dependencias y ofrece alternativas (marcar como inactivo, ver dependencias).
    1.B.2 El administrador decide la acción a seguir (cancelar, inactivar, gestionar dependencias).

4.A El proveedor posee compras asociadas.
    4.A.1 El sistema informa que no puede eliminarse físicamente.
    4.A.2 El sistema permite inactivarlo.


# Postcondiciones: proveedor marcado como inactivo en la base de datos.
# Escenarios de Éxito:
1. El administrador confirma la eliminación y el sistema la realiza, mostrando confirmación.
# Escenarios de Fracaso:
1. Eliminación rechazada por dependencias en la base de datos; no se elimina el proveedor.
2. El administrador cancela la operación y no se realizan cambios.