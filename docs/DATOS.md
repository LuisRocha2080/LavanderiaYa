# Modelo de datos — LavanderiaYa

Base SQLite local (`expo-sqlite`). Fechas en formato ISO `AAAA-MM-DD`; montos en bolivianos con dos decimales (guardados como enteros en centavos).

## `clientes`

Columnas: id, nombre, telefono, creado_en

## `servicios`

Columnas: id, nombre, precio_unidad, unidad (kg / prenda), activo

## `pedidos`

Columnas: id, numero, cliente_id, fecha_ingreso, fecha_prometida, estado, total, adelanto

## `pedido_items`

Columnas: id, pedido_id, servicio_id, cantidad, detalle

## `pagos`

Columnas: id, pedido_id, fecha, monto, metodo (efectivo / QR / transferencia)

## Reglas generales

- Cada tabla tiene `id` entero autoincremental.
- Los borrados con historial son **lógicos** (campo `activo`) para no romper reportes.
- Cambios de esquema mediante migraciones numeradas en `src/db/migraciones/`.
