---
name: cobranza
description: Cobranza en MateClim Service - trabajos terminados con saldo pendiente, total por cobrar, a quién cobrar primero, mensajes de recordatorio de pago y registro de pagos recibidos. Úsala cuando pidan "quién nos debe", cuentas por cobrar, cobranza o "ya pagó el cliente".
argument-hint: "[empresa]"
---

# Cobranza

Sigue las reglas de la skill `uso-mateclim`. Solo para administradores; si el rol no lo permite, dilo en una línea.

1. `mis_empresas` y `cuentas_por_cobrar`.
2. Presenta el **total por cobrar** y una tabla ordenada por antigüedad: folio, cliente, fecha de término, días y saldo. Destaca los 5 saldos más grandes o con más de 30 días.
3. Ofrece un mensaje de recordatorio por cliente para WhatsApp o correo: cordial, breve, con folio, monto y forma de pago. No lo envíes; entrégalo para copiar.
4. Si la persona dice que un cliente pagó, `registrar_cobro` con monto, forma de pago y quién recibió: vista previa sin `confirmado` → con aprobación, `confirmado: true`. El comprobante se adjunta en MateClim.
