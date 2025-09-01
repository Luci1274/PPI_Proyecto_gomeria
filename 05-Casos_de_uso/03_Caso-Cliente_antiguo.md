# Caso de uso: Registrar cliente antiguo
# Actores: Administrador
# Precondiciones: ...
# Caminos Basico:
1. El administrador ingresa a la pantalla cliente con antiguedad.
2. El sistema carga y muestra la pantalla.
3. El administrador hace click en "Registrar cliente antiguo". 
4. El sistema carga el formulario y lo visualiza.
5. El administrador rellena los datos (nombre, CUIT/CUIL, telefono, email).
6. El sistema valida los datos y los guarda.
7. El administrador regresa a la pantalla anterior. 
8. El sistema repite el paso 2.
9. El administrador puede hacer click en "Ver listado de clientes".
10. El sistema actualiza y visualiza la pantalla.
11. El administrador puede hacer click en cualquier cliente y modificarlo o eliminarlo y hace click en "Guardar". 
12. El sistema guarda los datos y muestra mensaje de exito. 

# Caminos Alternativos:
5 Si el administrador cancela el formulario.
    5.1 Regresa al paso 1. 

6 Error al validar los datos ingresados.
    6.1 El sistema informa sobre datos invalidos. 
    6.2 Regresa al paso 5. 

12 Error al validar los cambios realizados. 
    12.1 El sistema muestra error y los datos quedan intactos. 
    12.2 Regresa al paso 11.

# Postcondiciones: Cliente antiguo registrado correctamente y guardado en la base de datos 
# Escenarios de Exito:
# Escenarios de Exito: