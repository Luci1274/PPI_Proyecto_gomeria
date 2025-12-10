# Diccionario de datos 

## Venta

venta = fecha + hora + 1{ítem_venta}n + forma de pago + descuento + factura + iva + cantidad total de productos vendidos + precio_total.

forma de pago = [Efectivo | Tarjeta | Transferencia]

factura = [A | B] + fecha_emisión + número_factura

ítem_venta = nombre_producto + precio_unitario + cantidad

## Compra

compra = proveedor + 1{ítem_compra}n + forma_de_pago + fecha + hora + iva + cantidad_total_comprada + precio_total

forma de pago = [Efectivo | Tarjeta | Transferencia]

ítem_compra = nombre_producto + precio_unitario + cantidad

## Producto

producto = nombre + tipo + marca + precio_unitario + cantidad + historial_precio

stock = 1{producto}n + precio_unitario + cantidad + porcentaje_venta + historial_movimiento

historial_precio = nombre_producto + precio_unitario + fecha_inicio_vigencia + fecha_fin_vigencia

historial_movimiento = [ingreso y egreso]

ingreso = [compra de producto]

egreso = [venta de producto]

## Cliente con antigüedad

cliente = nombre + apellido + plazo de pago + deuda + historial de pago + historial de compra + forma de contacto

forma de contacto = [Teléfono | Email | Whatsapp]

historial de compras = 1{compra}n + fecha + hora + cantidad + precio_total

historial de pago = 1{pago}n + fecha + hora + monto + forma de pago

forma de pago = [Efectivo | Tarjeta | Transferencia]

## Proveedor

proveedor = dirección + forma de contacto + CUIT + Nombre

forma de contacto = [Teléfono | Email | Whatsapp]

## Tabla dato elemental producto

| Nombre | Descripción | Tipo de dato | Longitud | Dominio |
|:-------|:------------|:-------------|:---------|:--------|
| Nombre_producto|Nombre que recibe un producto|STR|30|Discreto|
| Tipo|Tipo de producto|STR|25|Discreto|
| Marca|Marca del producto|STR|25|Discreto|
| Precio unitario| Precio por unidad del producto|FLOAT|10|Continuo|
| Precio total| Precio total de compra o venta|FLOAT|10|Continuo|
| Stock| Cantidad disponible de productos|INT|100|Discreto|

## Tabla dato elemental cliente

| Nombre | Descripción | Tipo de dato | Longitud | Dominio |
|:-------|:------------|:-------------|:---------|:--------|
| Nombre | Nombre del cliente | STR | 15 | Discreto |
| Apellido | Apellido del cliente | STR | 15 | Discreto |
| Plazo de pago | Dias permitidos para pagar | INT | 2 | Discreto |
| Deuda | Saldo adeudado del cliente | FLOAT | 15 | Continuo |
| Historial de pago | Registro de pagos realizados | STR | 100 | Discreto |
| Historial de compra | Registro de compras realizadas. | STR | 100 | Discreto |
| Forma de contacto | Medio por el cual se contacta al cliente | STR | 20 | Discreto |

## Tabla dato elemental proveedor

| Nombre | Descripción | Tipo de dato | Longitud | Dominio |
|:-------|:------------|:-------------|:---------|:--------|
| CUIT | Identificación tributaria del proveedor | INT | 11 | Continuo |
| Forma de contacto | Medio de contacto del proveedor | STR | 20 | Discreto |
| Nombre | Nombre del proveedor o empresa | STR | 40 | Discreto |
