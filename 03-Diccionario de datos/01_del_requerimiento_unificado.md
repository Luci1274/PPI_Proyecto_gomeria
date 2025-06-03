# 01_del_requerimiento_unificado

## Venta

venta = fecha + hora + 1{item_venta}n +  forma de pago + descuento + factura + iva + cantidad total de productos vendidos + precio_total.

forma de pago = [Efectivo | Tarjeta | Transferencia]

factura = [A | B]

item_venta = nombre_producto + precio_unitario + cantidad

## Compra

compra = proveedor + 1{item_compra}n + forma_de_pago + fecha + hora + iva + cantidad_total_comprada + precio_total

forma de pago = [Efectivo | Tarjeta | Transferencia]

item_compra = nombre_producto + precio_unitario + cantidad

## Producto

producto = nombre + tipo + marca + precio_unitario + cantidad

stock = 1{producto}n + precio_unitario + cantidad + porcentaje_venta

## Proveedor

proveedor = direccion + telefono_movil + mail + CUIT

## Tabla dato elemental

| Nombre | Descripción | Tipo de dato | Longitud | Dominio |
|:-------|:------------|:-------------|:---------|:--------|
| CUIT|Es un codigo identificador de empresas|INT|11|Continua|
| Nombre_producto|Nombre que recibe un producto|STR|...|Discreto|
| Tipo|Tipo de producto|STR|..|Discreto|
| Marca|Marca del producto|STR|...|Disccreto|
| Precio| Precio del producto|Float|...|Continua|
| Stock| Cantidad de productos|INT|...|Continua|
