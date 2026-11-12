# Guía de contribución — LavanderiaYa

¡Gracias por querer aportar!

## Antes de empezar

1. Revisa el [roadmap](docs/ROADMAP.md) y el [backlog](docs/BACKLOG.md).
2. Abre un *issue* para discutir cambios grandes antes de escribir código.

## Flujo de trabajo

1. Haz un *fork* y crea una rama: `feat/nombre-corto` o `fix/nombre-corto`.
2. Instala dependencias: `npm install`.
3. Haz tus cambios con pruebas cuando toquen lógica de cálculo.
4. Verifica: `npm test` y `npx tsc --noEmit`.
5. Abre un *pull request* describiendo qué cambia y por qué.

## Mensajes de commit

Formato `tipo: descripción corta` en español. Tipos: `feat`, `fix`, `docs`, `refactor`, `test`, `chore`.

## Reglas del proyecto

- Todo debe funcionar sin conexión.
- No agregar dependencias con licencia de pago ni servicios con costo recurrente.
- Textos de interfaz en español.
