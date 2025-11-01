# Caso de uso: Registrar Compra
# Actores: Administrador
# Precondiciones: Tiene que haber un proveedor en el sistema

# Caminos Básico:
1. El administrador ingresa proveedor(Cuit, contacto).
2. El sistema guarda los datos.
3. El administrador ingresa forma de pago (Efectivo | Tarjeta | Transferencia). 
4. El sistema guarda los datos.
5. El administrador crea item de compra con (productos, tipo, marca, cantidad, precio unitario) y guarda los datos.
6. El sistema actualiza stock y guarda registro.


# Caminos Alternativos:
2.A Datos del proveedor no válidos.
    
    2.A.1 EL sistema muestra error y vuelve al paso 1

4.A Forma de pago inválida.

    4.A.1 El sistema muestra error y vuelve al paso 3.

6.A Datos del producto invalidos.

    6.A.1 El sistema muestra error y vuelve al paso 7.

# Postcondiciones: Compra registrada en el sistema.
# Escenarios de Éxito: 
1. Compra ingresada correctamente con todos los datos válidos. 
2. Stock de productos actualizado según cantidades compradas. 

# Escenarios de Fracaso:
1. Se ingresan cantidades negativas, precios nulos o productos inexistentes.
2. El administrador ingresa un método de pago invalido o incompleto. 
3. Por error del sistema o conflicto de datos, el stock no se actualiza correctamente después de guardar la compra. 