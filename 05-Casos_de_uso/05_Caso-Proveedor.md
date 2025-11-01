# Caso de uso: Registrar proveedor
# Actores: Administrador
# Precondiciones: ...
# Caminos Básico:
1. El administrador ingresa a la pantalla de Proveedor.
2. El sistema carga y muestra la pantalla.
3. El administrador hace click en "Registrar Proveedor". 
4. El sistema carga el formulario y lo visualiza.
5. El administrador rellena los datos (nombre, CUIT, teléfono, email).
6. El sistema valida los datos y los guarda.
7. El administrador regresa a la pantalla anterior. 
8. El sistema repite el paso 2.
9. El administrador puede hacer click en "Ver listado de proveedores".
10. El sistema actualiza y visualiza la pantalla.
 
# Caminos Alternativos:
3 Si el proveedor no desea registrar
    3.1 Puede hacer click en cualquier proveedor y modificarlo o eliminarlo y hace click en "Guardar". 
    3.2 El sistema guarda los datos y muestra mensaje de éxito.

5 Si el administrador cancela el formulario.
    5.1 Regresa al paso 1. 

6 Error al validar los datos ingresados.
    6.1 El sistema informa sobre datos inválidos. 
    6.2 Regresa al paso 5. 

12 Error al validar los cambios realizados. 
    12.1 El sistema muestra error y los datos quedan intactos. 
    12.2 Regresa al paso 11.

# Postcondiciones: proveedor registrado correctamente y guardado en la base de datos 
# Escenarios de Éxito:
6.1 El administrador completa todos los datos obligatorios de un proveedor y el sistema los valida y guarda correctamente.

7.1 El administrador cancela el formulario de registro y el sistema vuelve a la pantalla anterior sin errores.

10.1 El administrador accede al listado de proveedores, visualiza correctamente la información y selecciona un proveedor existente para modificarlo o eliminarlo, guardando los cambios exitosamente.

12.1 El sistema confirma con un mensaje que los datos se guardaron correctamente.
# Escenarios de Fracaso:
6.2 El administrador ingresa datos inválidos (ejemplo: CUIT mal formado, email con formato incorrecto, teléfono incompleto) y el sistema rechaza la operación mostrando un mensaje de error.

11.1 El administrador intenta modificar o eliminar un proveedor, pero los datos no pasan la validación; el sistema informa el error y no aplica los cambios.

12.1 Se produce un error de conexión con la base de datos al intentar guardar el proveedor y el sistema muestra un mensaje de fallo, sin guardar nada.

4.1 El administrador abandona el formulario sin guardarlo y se pierden los datos cargados (si no se implementa auto-guardado).
