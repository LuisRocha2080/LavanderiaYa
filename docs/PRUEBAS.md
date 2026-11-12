# Plan de pruebas — LavanderiaYa

## Automáticas (Jest)

La lógica de cálculo vive en `src/lib/` y se prueba sin interfaz.

- [ ] Totales y saldos con casos límite (adelanto = total, adelanto > total).
- [ ] Numeración correlativa tras borrar y reiniciar la app.
- [ ] Cierre de caja con pagos de días distintos.
- [ ] Mensaje de WhatsApp con teléfonos con y sin código de país (+591).
- [ ] Funcionamiento en modo avión.

## Manuales en teléfono real

- [ ] Instalación del APK en Android 10 o superior.
- [ ] Uso completo en modo avión.
- [ ] Cierre abrupto de la app y reapertura sin pérdida de datos.
- [ ] Exportación y apertura del archivo en otra app.

## Comandos

```bash
npm test
npx tsc --noEmit
```
