# 01_del_requerimiento_unificado

## Venta

venta = fecha + hora + 1{item_venta}n + forma de pago + descuento + factura + iva + cantidad total de productos vendidos + precio_total.

forma de pago = [Efectivo | Tarjeta | Transferencia]

factura = [A | B] + fecha_emision + numero_factura

item_venta = nombre_producto + precio_unitario + cantidad

## Compra

compra = proveedor + 1{item_compra}n + forma_de_pago + fecha + hora + iva + cantidad_total_comprada + precio_total

forma de pago = [Efectivo | Tarjeta | Transferencia]

item_compra = nombre_producto + precio_unitario + cantidad

## Producto

producto = nombre + tipo + marca + precio_unitario + cantidad + historial_precio

stock = 1{producto}n + precio_unitario + cantidad + porcentaje_venta + historial_movimiento

historial_precio = nombre_producto + precio_unitario + fecha_inicio_vigencia + fecha_fin_vigencia

historial_movimiento = [ingreso y egreso]

ingreso = [compra de producto]

egreso = [venta de producto]

## Cliente con antigüedad

cliente = nombre + apellido + plazo de pago + deuda + historial de pago + historial de compra + forma de contacto

forma de contacto = [Telefono | Email | Whatsapp]

historial de compras = 1{compra}n + fecha + hora + cantidad + precio_total

historial de pago = 1{pago}n + fecha + hora + monto + forma de pago

forma de pago = [Efectivo | Tarjeta | Transferencia]

## Proveedor

proveedor = direccion + forma de contacto + CUIT

forma de contacto = [Telefono | Email | Whatsapp]

## Tabla dato elemental producto

| Nombre | Descripción | Tipo de dato | Longitud | Dominio |
|:-------|:------------|:-------------|:---------|:--------|
| CUIT|Es un codigo identificador de empresas|INT|11|Continuo|
| Nombre_producto|Nombre que recibe un producto|STR|30|Discreto|
| Tipo|Tipo de producto|STR|25|Discreto|
| Marca|Marca del producto|STR|25|Discreto|
| Precio unitario| Precio unitario del producto|FLOAT|10|Continuo|
| Precio total| Precio total de la compra y/o venta|FLOAT|10|Continuo|
| Stock| Cantidad de productos|INT|100|Continuo|

## Tabla dato elemental cliente

| Nombre | Descripción | Tipo de dato | Longitud | Dominio |
|:-------|:------------|:-------------|:---------|:--------|
| Nombre | Nombre del cliente | STR | 15 | Discreto |
| Apellido | Apellido del cliente | STR | 15 | Discreto |
| Plazo de pago | plazo de 30 dias para pagar | INT | 2 | Discreto |
| Deuda | Deuda del cliente | FLOAT | 15 | Continuo |
| Historial de pago | Historial de pago del cliente | STR | 100 | Discreto |
| Historial de compra | Historial de compra del cliente | STR | 100 | Discreto |
| Forma de contacto | Forma de contacto del cliente | STR | 20 | Discreto |

## Tabla dato elemental proveedor

| Nombre | Descripción | Tipo de dato | Longitud | Dominio |
|:-------|:------------|:-------------|:---------|:--------|
| CUIT | Código único de identificación tributaria | INT | 11 | Continuo |
| Forma de contacto | Forma de contacto del cliente | STR | 20 | Discreto |
