---
name: nuevo-servicio
description: Da de alta en MateClim Service un mantenimiento, instalación, visita o diseño con cliente, fecha, hora y técnico, y avisa al técnico. Úsala cuando pidan "agenda un mantenimiento", "programa una visita" o "da de alta un servicio".
argument-hint: "<qué, para quién y cuándo>"
disable-model-invocation: true
---

# Nuevo servicio

Sigue las reglas de la skill `uso-mateclim`.

1. Toma de $ARGUMENTS y de la conversación: cliente, tipo (mantenimiento, instalación, visita o diseño), fecha, hora, técnico, dirección, teléfono, equipo y descripción.
2. `mis_empresas` para la empresa. Si el cliente puede existir, `buscar_cliente` y usa su nombre exacto. Si no dijeron técnico y la persona es administradora, `tecnicos` para sugerir al de menos carga.
3. Pregunta solo lo indispensable que falte: cliente, tipo y fecha.
4. `crear_servicio` sin `confirmado` → muestra la vista previa → con aprobación, `confirmado: true`.
5. Responde con el folio y a quién se avisó.
