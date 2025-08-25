# Caso de uso: Registrar Compra
# Actores: Administrador
# Precondiciones:

# Caminos Basico:
1. El administrador ingresa proveedor.
2. El sistema guarda los datos.
3. El administrador ingresa forma de pago. 
4. El sistema guarda los datos.
5. El administrador seleccionar item de compra
6. El sistema visualiza el item de compra.
7. El administrador registra productos, cantidad, precio unitario y guarda los datos.
8. El administrador guarda los datos.
9. El sistema guarda los datos.
10. El sistema visualiza la informacion ingresada.
11. El sistema actualiza stock y guarda registro.
12. El administrador presiona Listado de compras.
13. El sistema visualiza listado de compras.
14. El administrador modifica los datos ingresados.
15. El sistema valida los datos.
16. El sistema valida correctamente y visualiza los cambios en el listado. 
17. El administrador filtra listado de compra.
18. El sistema filtra y visualiza los resultados. 

# Caminos Alternativos:
1.A Datos del proveedor no validos.
1.A.1 EL sistema muestra error y vuelve al paso 1
3.A Forma de pago invalida.
3.A.1 El sistema muestra error y vuelve al paso 3.
7.A Datos del producto invalidos.
7.A.1 El sistema muestra error y vuelve al paso 7.
14.A Datos de modificacion invalidos.
14.A.1 El sistema muestra error y vuelve al paso 14
17.A Datos de filtrado invalidos.
17.A.1 El sistema muestra error y vuelve al paso 17.

# Postcondiciones: Compra registrada en el sistema.
# Escenarios de Exito: 
1. Compra ingresada correctamente con todos los datos validos. 
2. Stock de productos actualizado segun cantidades ingresadas. 
3. Registro disponible en el listado de compras.
4. Modificaciones realizadas por el administrador reflejadas correctamente en el listado. 
5. Filtrado de compras funciona correctamente segun criterios.
# Escenarios de Fracaso:
1. Se ingresan cantidades negativas, precios nulos o productos inexistentes.
2. El administrador ingresa un metodo de pago invalido o incompleto. 
3. Por error del sistema o conflicto de datos, el stock no se actualiza correctamente despues de guardar la compra. 
4. El administrador intenta modificar la compra con datos que no cumplen las reglas de validacion (cantidad negativa, producto inexistente, etc.)
5. El listado de compras no se actualiza correctamente o no muestra los registros debido a algun error en la consulta o filtrado.
