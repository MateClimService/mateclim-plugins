---
name: cotizar
description: Crea una cotización en MateClim Service con partidas (nombre, unidad, cantidad y precio en MXN o USD) a partir de una lista, un levantamiento o una foto, con total e IVA, y entrega el enlace del PDF. Úsala cuando pidan "cotiza", "arma una cotización" o "pasa esto a cotización".
argument-hint: "<cliente y conceptos>"
disable-model-invocation: true
---

# Cotizar

Sigue las reglas de la skill `uso-mateclim`. El conector entrega el PDF de la cotización.

1. Reúne: cliente (y su empresa, teléfono, dirección o RFC si los dio), asunto y partidas. Pueden venir en $ARGUMENTS, en la conversación o en un archivo adjunto.
2. Si es una instalación, un cambio o una desinstalación de equipo, propón desglosado todo lo que lleva el trabajo (refrigerante, tubería, conexiones, soldadura, aislamiento, presurizado, vacío, limpieza, soportería, mano de obra, maniobras) y marca lo que agregaste para que lo confirmen o lo quiten.
3. Cada partida: nombre, unidad (`pza` o `m`), cantidad y precio unitario **antes de IVA**. Busca primero el precio en `catalogo`; si no está y no lo dieron, pregúntalo; no lo inventes. Si los dieron con IVA, divide entre 1.16 y avísalo.
4. Un precio en dólares va con `moneda: USD`, sin convertirlo, y pide el tipo de cambio (`tipo_cambio_usd`).
5. `mis_empresas` para la empresa; `buscar_cliente` si el cliente puede existir.
6. `crear_cotizacion` sin `confirmado` → muestra partidas, subtotal, IVA y total (ninguna partida sin nombre) → con aprobación, `confirmado: true`.
7. Responde con el folio y el enlace para descargar el PDF, no el de la pantalla. Si lo piden después, usa `pdf_cotizacion`. Usa `con_iva: false` solo si lo piden.
