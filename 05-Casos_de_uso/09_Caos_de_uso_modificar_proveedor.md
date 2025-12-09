# Caso de uso: Modificar proveedor
# Actores: Administrador
# Precondiciones: Caso de uso 05 Listado de proveedores. El proveedor existe y está seleccionado desde el listado.
# Caminos Básico:

1. El administrador selecciona un proveedor en el listado y elige "Modificar proveedor".
2. El sistema muestra el formulario con los datos actuales del proveedor.
3. El administrador modifica los campos necesarios (nombre, CUIT, teléfono, email, estado).
4. El sistema valida los datos y guarda los cambios.
5. El sistema regresa al caso de uso 05 y actualiza la lista mostrando los cambios.

# Caminos Alternativos:
1.A Error al validar los datos ingresados.
    
    1.A.1 El sistema informa sobre los campos inválidos.
    1.A.2 Regresa al paso 3 para corrección.

1.B Edición cancelada o formulario cerrado.
    
    1.B.1 El sistema descarta cambios y regresa al caso de uso 05 sin guardar.

1.C Conflicto de concurrencia (otro usuario modificó el proveedor).
    
    1.C.1 El sistema informa del conflicto y ofrece opciones: recargar datos, sobrescribir o cancelar.
    1.C.2 Según la elección, vuelve al paso 2 o 1.B.

# Postcondiciones: proveedor modificado correctamente y los cambios guardados en la base de datos; la lista refleja la modificación.
# Escenarios de Éxito:
1. El administrador modifica datos válidos y el sistema los guarda, mostrando un mensaje de confirmación.
# Escenarios de Fracaso:
1. Datos inválidos rechazados por validación; la operación no se completa.
2. Error de conexión a la base de datos al guardar; el sistema muestra mensaje de fallo y no guarda cambios.
3. Conflicto de concurrencia que impide guardar hasta resolución.