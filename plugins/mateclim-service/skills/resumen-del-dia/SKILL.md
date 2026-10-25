---
name: resumen-del-dia
description: Resumen del día en MateClim Service - trabajos de hoy, atrasados, en proceso y sin técnico. Úsala cuando pidan "resumen de hoy", "qué hay hoy", "cómo vamos" o el arranque del día.
argument-hint: "[empresa]"
---

# Resumen del día

Sigue las reglas de la skill `uso-mateclim`. Este comando solo consulta.

1. `mis_empresas`; usa la empresa de $ARGUMENTS o todas las de la persona.
2. Por empresa: `agenda` con `desde` y `hasta` = hoy (hora de México) y `pendientes`.
3. Presenta por empresa:
   - **Hoy:** hora, folio, cliente, tipo y técnico. Marca los que no tienen técnico.
   - **Atrasados:** programados antes de hoy que siguen abiertos.
   - **En proceso** y **por confirmar**.
   - Al final, lo más urgente en máximo 3 puntos.
4. Si una herramienta falla, dilo en una línea y sigue con lo demás. Si la persona es instalador, verá solo sus trabajos; preséntalo como «tus trabajos».
