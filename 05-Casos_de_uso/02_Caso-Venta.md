# Caso de uso: Venta
# Actores: usuario (vendedor)
# Precondiciones: ... 
# Caminos Basico:
1. El usuario ingresa al sistema.
2. El usuario selecciona la opción de "Realizar Venta".
3. El sistema muestra el formulario de venta.
4. El usuario ingresa los detalles de la venta (fecha, froma de pago, descuento, factura, iva).
5. El usuario hace click en "Agregar item venta".
6. El sistema muestra el formulario para agregar un item a la venta(nombe_producto, precio unitario, cantidad), el usuario hace click en aceptar.
7. El sistema agrega el item a la venta y muestra el total actualizado.
8. El usuario puede repetir el paso 5 para agregar más items o hacer click en "Finalizar Venta".
9. El sistema muestra un resumen de la venta
10. el usuario puede hacer click en cualquier item de venta y modificarla o eliminarla.
11. El usuario hace click en "Confirmar Venta".
12. El sistema guarda la venta y muestra un mensaje de éxito.
13. El usuario puede imprimir el ticket de la venta o ver el historial de ventas.

# Caminos Alternativos:
6_1. Si el usuario decide cancelar la adición de un item, puede hacer click en "Cancelar" y volver al formulario de venta sin agregar el item.

7_1. Si el usuario ingresa un item con un nombre de producto que no existe, el sistema muestra un mensaje de error y no agrega el item a la venta.

8_1 Si el usuario decide cancelar la venta, puede hacer click en "Cancelar Venta" y volver al formulario de venta sin guardar nada.

# Postcondiciones: 
El sistema guarda la venta en la base de datos y actualiza el inventario de productos.

# Escenarios de Exito:
El sistema permite al usuario realizar una venta de manera exitosa, guardando todos los detalles y actualizando el inventario. El usuario puede imprimir el ticket de la venta o ver el historial de ventas.

# Escenarios de Fracaso:
El sistema no permite al usuario realizar una venta si hay errores en los detalles ingresados (por ejemplo, si el nombre del producto no existe o si la cantidad es negativa). En estos casos, el sistema muestra mensajes de error y no guarda la venta. El usuario puede corregir los errores y volver a intentar la venta.