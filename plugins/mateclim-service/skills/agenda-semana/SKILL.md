---
name: agenda-semana
description: Agenda de la semana en MateClim Service por técnico - trabajos programados, días cargados, choques de horario y trabajos sin asignar. Úsala cuando pidan la agenda, "qué tiene Juan esta semana", reprogramar o repartir trabajo.
argument-hint: "[técnico]"
---

# Agenda de la semana

Sigue las reglas de la skill `uso-mateclim`.

1. `mis_empresas` para la empresa.
2. `agenda` de hoy a 7 días después; si mencionaron un técnico ($ARGUMENTS), pásalo en `tecnico`.
3. Si la persona es administradora, `tecnicos` para ver cuántos trabajos abiertos tiene cada uno.
4. Muestra una tabla por día (hora, folio, cliente, técnico) y después: trabajos **sin técnico**, técnicos con **dos trabajos a la misma hora** o más de 3 en un día, y técnicos **libres**.
5. Si piden mover o asignar, propón el cambio y usa `reprogramar` o `asignar_tecnico` con vista previa y confirmación.
