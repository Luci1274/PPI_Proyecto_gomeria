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

## Proveedor

proveedor = direccion + telefono_movil + mail + CUIT

## Tabla dato elemental

| Nombre | Descripción | Tipo de dato | Longitud | Dominio |
|:-------|:------------|:-------------|:---------|:--------|
| CUIT|Es un codigo identificador de empresas|INT|11|Continuo|
| Nombre_producto|Nombre que recibe un producto|STR|30|Discreto|
| Tipo|Tipo de producto|STR|25|Discreto|
| Marca|Marca del producto|STR|25|Discreto|
| Precio unitario| Precio unitario del producto|FLOAT|10|Continuo|
| Precio total| Precio total de la compra y/o venta|FLOAT|10|Continuo|
| Stock| Cantidad de productos|INT|100|Continuo|
