# 01_del_requerimiento_unificado

## Venta

venta = fecha + hora + 1{item_venta}n +  forma de pago + descuento + factura + iva + cantidad total de productos vendidos + precio_total.

forma de pago = [Efectivo | Tarjeta | Transferencia]

factura = [A | B]

item_venta = @Id_producto + nombre_producto + precio_unitario + 1{cantidad}n

## Compra

compra = proveedor + 1{item_compra}n + forma_de_pago + fecha + hora+ iva + cantidad_total_comprada + precio_total

forma de pago = [Efectivo | Tarjeta | Transferencia]

item_compra = @Id_producto + nombre_producto + precio_unitario + 1{cantidad}n

## Productos

productos = @Id_producto + nombre + tipo + marca + precio_unitario + 0{cantidad}n

stock = 1{producto}n + precio_unitario + 0{cantidad}n + + porcentaje_venta

## Proveedor

proveedor = nombre + apellido + direccion + telefono_movil + mail + dni

## Tabla dato elemental

| Nombre | Descripción | Tipo de dato | Longitud | Dominio |
|:-------|:------------|:-------------|:---------|:--------|
| Id_producto | Numero identificador de cada producto | INT | ..... | Continua |