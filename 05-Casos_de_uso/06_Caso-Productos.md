
# Caso de uso: Productos

# Actores: Administrador

# Precondiciones: 
El actor debe haber iniciado sesión en el sistema.
El producto no debe estar previamente registrado.

# Caminos Básico:
1. El administrador selecciona la opción "registrar producto"
2. El sistema muestra un formulario de registro
3. El administrador completa los datos del producto(nombre, cantidad, precio)
4. El administrador confirma la operación
5. El sistema valida los datos
6. El sistema guarda el producto registrado en la BBDD
7. El sistema muestra un mensaje de confirmación
8. El administrador consulta la lista de productos
9. El sistema muestra los productos en stock y los faltantes
10. El administrador modifica los precios de los productos
11. El sistema actualiza los precios
12. El sistema muestra un mensaje de éxito
13. El sistema descuenta el producto vendido
14. El sistema actualiza la cantidad de stock
15. El administrador elimina los productos que no vende más
16. El sistema actualiza la lista de productos

# Caminos Alternativos:
1. Si el producto ya existe, el sistema notifica y ofrece la opción de registrar nuevo producto.
2. Si faltan datos obligatorios, el sistema muestra un mensaje de error y solicita completar la información.
3. Si ocurre un error en la base de datos, el sistema informa que no fue posible registrar el producto.

# Postcondiciones: 
El producto queda registrado en el sistema con todos sus datos.

# Escenarios de Éxito: 
El producto se registra correctamente y está disponible para ser gestionado (consultado, vendido o modificado).

# Escenarios de Fracaso: 
El producto no se registra porque ya existe, faltan datos o ocurre un error en el sistema.
