---
name: registrar-compra
description: Registra en MateClim Service la compra de materiales de un folio o un gasto de la empresa (sueldo, gasolina o general) leyendo el ticket o la factura. Úsala cuando manden la foto o el PDF de un ticket o factura, o digan "registra este gasto" o "carga este material al folio".
argument-hint: "[folio]"
disable-model-invocation: true
---

# Registrar compra o gasto

Sigue las reglas de la skill `uso-mateclim`.

1. Lee el comprobante adjunto: proveedor, fecha, número del ticket, UUID si es factura, partidas (descripción, cantidad, precio unitario, subtotal) y total con IVA. Lo que no se lea, pregúntalo.
2. Destino:
   - **Material de un trabajo** (hay folio en $ARGUMENTS o en la conversación): `registrar_material`.
   - **Gasto de la empresa sin folio:** `registrar_gasto` (solo administración).
3. Pregunta lo que falte: quién pagó, contado o crédito, y forma de pago (con tarjeta, su nombre).
4. Vista previa sin `confirmado` → con aprobación, `confirmado: true`.
5. Recuerda que la foto del comprobante se adjunta en MateClim; ofrece `enlace_subir_fotos` si es material de un folio.
