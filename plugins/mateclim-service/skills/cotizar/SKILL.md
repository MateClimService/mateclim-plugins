---
name: cotizar
description: Crea una cotización en MateClim Service con partidas (nombre, unidad, cantidad y precio en MXN) a partir de una lista, un levantamiento o una foto, con total e IVA. Úsala cuando pidan "cotiza", "arma una cotización" o "pasa esto a cotización".
argument-hint: "<cliente y conceptos>"
disable-model-invocation: true
---

# Cotizar

Sigue las reglas de la skill `uso-mateclim`. El PDF y el envío al cliente se hacen después en MateClim.

1. Reúne: cliente (y su empresa, teléfono, dirección o RFC si los dio), asunto y partidas. Pueden venir en $ARGUMENTS, en la conversación o en un archivo adjunto.
2. Cada partida: nombre, unidad (`pza` o `m`), cantidad y precio unitario en MXN **antes de IVA**. Si no dieron precios, pregúntalos; no los inventes. Si los dieron con IVA, divide entre 1.16 y avísalo.
3. `mis_empresas` para la empresa; `buscar_cliente` si el cliente puede existir.
4. `crear_cotizacion` sin `confirmado` → muestra partidas, subtotal, IVA y total → con aprobación, `confirmado: true`.
5. Responde con el folio y recuerda que el PDF se descarga en Cotizaciones. Usa `con_iva: false` solo si lo piden.
