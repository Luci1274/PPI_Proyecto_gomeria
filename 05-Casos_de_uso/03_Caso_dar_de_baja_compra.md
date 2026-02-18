# Caso de uso: Dar de baja compra
# Actores: Administrador
# Precondiciones:La compra debe existir en el sistema, La compra no debe encontrarse en estado Anulada..

# Caminos Básico:
1. El Administrador selecciona la compra.
2. El sistema verifica que la compra no esté anulada.
3. El sistema solicita confirmación.
4. El Administrador ingresa el motivo.
5. El sistema valida el motivo.
6. El sistema cambia el estado de la compra a Anulada.
7. El sistema revierte el stock de los productos asociados.

# Caminos Alternativos:
4.A Motivo inválido o vacío
    4.A.1 El sistema muestra mensaje de error "El motivo no puede estar vacío".
    4.A.2 El administrador ingresa un motivo válido.

7.A El stock no puede ser revertido
    7.A.1 El sistema muestra mensaje de error "No se pudo revertir el stock, contacte al soporte".
    7.A.2 El administrador contacta al soporte para resolver el problema.

# Postcondiciones: La compra queda en estado Anulada, El stock de los productos es actualizado.
# Escenarios de Éxito:
1. La compra es dada de baja correctamente con un motivo válido.
2. El sistema actualiza el estado de la compra y refleja el cambio en el listado.
# Escenarios de Fracaso:
1. La compra ya estaba dada de baja; el sistema informa al administrador.
2. El motivo ingresado es inválido o vacío; el sistema no permite dar de baja la compra hasta que se ingrese un motivo válido.
