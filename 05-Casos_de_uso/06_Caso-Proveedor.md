# Caso de uso: Registrar proveedor
# Actores: Administrador
# Precondiciones: Caso de uso 05 Listado de proveedores
# Caminos Básico:

1. El administrador rellena los datos (nombre, CUIT, teléfono, email).
2. El sistema valida los datos y los guarda.
3. El sistema regresa al caso de uso 05
 
# Caminos Alternativos:
1.A Error al validar los datos ingresados.
    1.A.1 El sistema informa sobre datos inválidos. 
    1.A.2 Regresa al paso 1.

1.B Formulario cerrado
    1.B.1 El sistema regresa al caso de uso 05 sin guardar datos.

# Postcondiciones: proveedor registrado correctamente y guardado en la base de datos 
# Escenarios de Éxito:
1. El administrador completa todos los datos obligatorios de un proveedor y el sistema los valida y guarda correctamente.

2. El sistema confirma con un mensaje que los datos se guardaron correctamente.
# Escenarios de Fracaso:
1. El administrador ingresa datos inválidos (ejemplo: CUIT mal formado, email con formato incorrecto, teléfono incompleto) y el sistema rechaza la operación mostrando un mensaje de error.

2. Se produce un error de conexión con la base de datos al intentar guardar el proveedor y el sistema muestra un mensaje de fallo, sin guardar nada.

3. El administrador abandona el formulario sin guardarlo y se pierden los datos cargados.
