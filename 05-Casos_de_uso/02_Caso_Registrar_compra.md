# Caso de uso: Registrar Compra
# Actores: Administrador
# Precondiciones: Debe existir al menos un proveedor registrado en el sistema, debe existir el listado de compras.

# Caminos Básico:
1. El administrador ingresa nombre del proveedor y selecciona la forma de pago (Efectivo | Tarjeta | Transferencia).
2. El sistema valida y guarda los datos iniciales de la compra. 
3. El administrador registra un ítem de compra ingresando: (productos, tipo, marca, cantidad y  precio unitario).
4. El sistema valida la información, guarda el ítem y actualiza el stock del producto.

# Caminos Alternativos:
1.A Ingreso invalido de proveedor o forma de pago.
    
    1.A.1 EL sistema muestra error
    1.A.2 Vuelve al paso 1

3.A Datos del producto invalidos.

    3.A.1 El sistema muestra error 
    3.A.2 Vuelve al paso 3.

# Postcondiciones: Compra registrada en el sistema.
# Escenarios de Éxito: 
1. Compra ingresada correctamente con todos los datos válidos. 
2. Stock de productos actualizado según cantidades compradas. 

# Escenarios de Fracaso:
1. Se ingresan cantidades negativas, precios nulos o productos inexistentes.
2. El administrador ingresa un método de pago invalido o incompleto. 
3. Por error del sistema o conflicto de datos, el stock no se actualiza correctamente después de guardar la compra. 