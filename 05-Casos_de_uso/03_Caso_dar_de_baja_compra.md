# Caso de uso: Dar de baja compra
# Actores: Administrador
# Precondiciones: Debe existir un listado de compras en el sistema, y la compra a dar de baja no debe estar ya dada de baja.

# Caminos Básico:
1. El administrador selecciona la compra a dar de baja.
2. El sistema muestra la confirmación para dar de baja la compra.
3. El administrador ingresa el motivo.
4. El sistema valida el motivo y da de baja la compra, actualizando el estado en el sistema.

# Caminos Alternativos:
1.A Compra ya dada de baja
    1.A.1 El sistema muestra mensaje "La compra ya está dada de baja".
    1.A.2 El administrador puede regresar al listado de compras.

3.A Motivo inválido o vacío
    3.A.1 El sistema muestra mensaje de error "El motivo no puede estar vacío".
    3.A.2 El administrador ingresa un motivo válido.

# Postcondiciones: La compra queda registrada como dada de baja en el sistema con el motivo correspondiente.
# Escenarios de Éxito:
1. La compra es dada de baja correctamente con un motivo válido.
2. El sistema actualiza el estado de la compra y refleja el cambio en el listado.
# Escenarios de Fracaso:
1. La compra ya estaba dada de baja; el sistema informa al administrador.
2. El motivo ingresado es inválido o vacío; el sistema no permite dar de baja la compra hasta que se ingrese un motivo válido.
