# Caso de uso: Registrar Compra
# Actores: Administrador
# Precondiciones: Debe existir al menos un proveedor registrado en el sistema.

# Caminos Básico:
1. El Administrador selecciona proveedor y forma de pago.
2. El sistema crea una compra en estado Pendiente.
3. El Administrador ingresa uno o más ítems de compra.
4. El sistema valida y registra los ítems.
5. El Administrador confirma la compra.
6. El sistema registra la compra y actualiza el stock.


# Caminos Alternativos:
1.A Ingreso invalido de proveedor o forma de pago.
    
    1.A.1 EL sistema muestra error
    1.A.2 Vuelve al paso 1

3.A Ingreso de ítems con datos inválidos (cantidades negativas, precios nulos, productos inexistentes).
    3.A.1 El sistema muestra error indicando el problema específico.
    3.A.2 El administrador corrige los datos y vuelve al paso 3.

5.A Confirmación cancelada por el administrador.
    5.A.1 El sistema cancela el proceso de registro de compra.

# Postcondiciones: Compra registrada en el sistema.
# Escenarios de Éxito: 
1. Compra ingresada correctamente con todos los datos válidos. 
2. Stock de productos actualizado según cantidades compradas. 

# Escenarios de Fracaso:
1. Se ingresan cantidades negativas, precios nulos o productos inexistentes.
2. El administrador ingresa un método de pago invalido o incompleto. 
3. Por error del sistema o conflicto de datos, el stock no se actualiza correctamente después de guardar la compra. 