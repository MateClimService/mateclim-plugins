---
name: folio
description: Consulta un folio de MateClim Service (servicio, proyecto, servicio de tienda, iguala o cotización) - estado, cliente, técnico, fechas, reporte, fotos, materiales y pago, con el siguiente paso. Úsala cuando la persona mencione un folio o pregunte cómo va un trabajo.
argument-hint: "<folio>"
---

# Consultar un folio

Sigue las reglas de la skill `uso-mateclim`. Este comando solo consulta.

1. El folio es $ARGUMENTS; si no lo dio, pídelo. Identifica la empresa por el prefijo con `mis_empresas`.
2. `detalle_folio` con el folio exacto. Si no aparece, `buscar_folio`. Si preguntan por lo que se ha hecho, `historial_folio`; por lo gastado, `materiales_folio`; en proyectos, `avances_proyecto`.
3. Responde en este orden: estado, cliente y lugar, técnico, fechas, qué falta (reporte, fotos, firma, materiales, cobro) y el **siguiente paso** en una línea. Los montos solo aparecen si la persona es administradora.
4. Si piden un cambio (estado, fecha, técnico, datos), usa la herramienta correspondiente con vista previa y confirmación.
