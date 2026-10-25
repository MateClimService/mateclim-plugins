---
name: uso-mateclim
description: Cómo trabajar con MateClim Service desde Claude - empresas, folios, roles, estados de los trabajos y la regla de vista previa y confirmación antes de guardar. Úsala siempre que la persona pregunte o pida algo sobre sus servicios, proyectos, tiendas, igualas, cotizaciones, técnicos, materiales, reportes o cobros de MateClim, aunque no diga "MateClim".
---

# Trabajar con MateClim Service

MateClim Service es la plataforma donde la empresa de la persona lleva servicios de aire acondicionado y refrigeración, proyectos, tiendas, cotizaciones, materiales, reportes y cobros. Claude trabaja en ella con el conector **MateClim**, con la cuenta y los permisos de la persona.

## Antes de empezar

- Si las herramientas de MateClim no aparecen, pide a la persona que conecte «mateclim» en la pestaña Conectores del plugin e inicie sesión con su cuenta de MateClim. Para registrar cosas debe autorizar «consulta y registro»; si solo autorizó consulta, el conector lo dirá.
- Llama primero `mis_empresas`: da el identificador de cada empresa y el rol de la persona en ella. Si tiene una sola empresa, úsala sin preguntar.

## Reglas

1. **Nada se guarda sin aprobación.** Toda herramienta que crea, cambia o borra se llama primero sin `confirmado` para obtener la vista previa. Muéstrala completa y llama otra vez con `confirmado: true` solo si la persona dice que sí.
2. **Borrar solo si la persona lo pide con esas palabras** (borrar, eliminar). Avisa que no se puede deshacer.
3. **No inventes datos.** Precios, montos, fechas, folios, técnicos y clientes salen de la persona o de MateClim. Si falta algo indispensable, pregúntalo en una sola pregunta.
4. **Respeta el rol.** Si una herramienta responde que el rol no lo permite, explícalo en una línea; no busques otra forma de hacerlo.
5. **Folios exactos.** Los folios llevan el prefijo de la empresa y el tipo, por ejemplo `ABC-MNT-0012` (mantenimiento), `ABC-INS-0003` (instalación), `ABC-VIS-0020` (visita) o `PROY-ABC-0004` (proyecto). Si la persona da uno incompleto, búscalo con `buscar_folio`.
6. **Lo que se hace en la app:** fotos, firma del cliente, PDF de cotizaciones y reportes, y comprobantes. Para fotos, `enlace_subir_fotos` da el enlace directo al folio.

## Cómo responder

- Español de México, claro y breve. Fechas como «25 oct» y horas como «4:30 pm»; a las herramientas, AAAA-MM-DD y 24 h.
- Tablas cortas cuando hay varios trabajos; siempre con el folio.
- Al terminar algo que guardó, di qué quedó registrado y el folio. Si la herramienta devuelve un enlace, compártelo.
- Para dudas de la plataforma, pagos de la suscripción o fallas: soporte de MateClim en matriz@mateclim.com.
