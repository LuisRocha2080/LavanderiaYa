# Especificación — LavanderiaYa

Requisitos escritos con el patrón EARS («Cuando…, el sistema deberá…»). Cada uno es verificable con una prueba (ver [PRUEBAS.md](PRUEBAS.md)).

## Alcance de la versión 1.0

Pedidos de lavandería y tintorería con ticket numerado, estados, saldos por cobrar y aviso por WhatsApp. Funciona en un solo dispositivo, sin cuentas de usuario y sin servidor.

## Requisitos funcionales

| ID | Requisito |
|---|---|
| R01 | Cuando el usuario guarda un pedido, el sistema deberá asignarle un número correlativo único que no se reutilice. |
| R02 | Cuando se agregan items a un pedido, el sistema deberá calcular el total como la suma de cantidad × precio de cada servicio. |
| R03 | Cuando el usuario registra un pago, el sistema deberá actualizar el saldo del pedido y rechazar montos mayores al saldo. |
| R04 | Cuando un pedido pasa a «listo», el sistema deberá ofrecer enviar un mensaje de WhatsApp prellenado al teléfono del cliente. |
| R05 | Mientras un pedido esté «listo» por más de 7 días, el sistema deberá mostrarlo en la lista de atrasados. |
| R06 | Cuando se cierra la caja del día, el sistema deberá sumar solo los pagos cobrados en esa fecha, sin contar saldos pendientes. |
| R07 | Si el dispositivo no tiene conexión, el sistema deberá seguir registrando pedidos y pagos sin pérdida de datos. |
| R08 | Cuando el usuario solicita exportar, el sistema deberá generar un archivo CSV de pedidos y pagos del rango elegido. |

## Requisitos no funcionales

| ID | Requisito |
|---|---|
| N01 | La app deberá abrir en menos de 3 segundos en un teléfono Android de gama baja (2 GB de RAM). |
| N02 | Todos los datos deberán almacenarse en SQLite local y no enviarse a ningún servidor. |
| N03 | La interfaz deberá estar en español con montos en bolivianos (Bs) y fechas dd/mm/aaaa. |
| N04 | Los botones táctiles deberán medir al menos 48 dp. |
| N05 | La app deberá operar completa sin conexión a internet. |
| N06 | El costo de licencias de cualquier dependencia deberá ser cero. |

## Fuera de alcance (v1.0)

- Un solo dispositivo por negocio: los datos no se sincronizan entre teléfonos.
- No imprime tickets físicos en la primera versión.
- Sin facturación electrónica: emite notas de venta internas, no facturas del SIN.

## Criterios de aceptación globales

1. Un usuario nuevo registra su primer dato útil en menos de 5 minutos.
2. Ningún dato se pierde al cerrar la app de forma abrupta.
3. Los totales coinciden con un cálculo manual en los casos de prueba de [PRUEBAS.md](PRUEBAS.md).
