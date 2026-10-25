---
name: reporte-servicio
description: Redacta y guarda el reporte de un servicio en MateClim Service a partir de las notas, audios transcritos o fotos del técnico - condición antes, trabajos realizados, piezas cambiadas y recomendaciones. Úsala cuando digan "haz el reporte", "pasa esto al reporte" o terminen un trabajo.
argument-hint: "<folio>"
disable-model-invocation: true
---

# Reporte de servicio

Sigue las reglas de la skill `uso-mateclim`. Sirve para servicios, servicios de tienda e igualas; en proyectos se usan avances (`registrar_avance`).

1. Folio en $ARGUMENTS o pídelo. `detalle_folio` para confirmar equipo, cliente y lo que ya tiene el reporte.
2. Con las notas de la persona (texto, lista o fotos que describa), redacta en lenguaje técnico claro y sin exagerar:
   - **Condición antes:** cómo se encontró el equipo.
   - **Trabajos realizados:** qué se hizo, en orden.
   - **Piezas cambiadas:** pieza y cantidad, o «ninguna».
   - **Recomendaciones:** lo que el cliente debe hacer o programar.
   - **Resumen:** dos o tres líneas para el cliente.
   No agregues mediciones, piezas ni fallas que la persona no mencionó.
3. `guardar_reporte` sin `confirmado` → muestra el texto → con aprobación, `confirmado: true`.
4. Recuerda que las fotos y la firma del cliente se agregan en MateClim y ofrece `enlace_subir_fotos`.
