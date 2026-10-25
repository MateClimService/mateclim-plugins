# MateClim Service para Claude

Plugin para empresas que usan MateClim Service. Versión 1.0.0.

Conecta Claude con tu cuenta de MateClim para consultar y registrar el trabajo de tu empresa. Claude entra con tu usuario y solo puede ver y hacer lo que tu rol permite. Antes de guardar cualquier cosa te muestra lo que va a registrar y espera tu «sí».

## Qué incluye

- **Conector MateClim:** la conexión segura con tu cuenta.
- **uso-mateclim:** las reglas para trabajar con tus folios, roles y confirmaciones.
- **Comandos:**

| Comando | Qué hace |
| --- | --- |
| `/resumen-del-dia` | Trabajos de hoy, atrasados, en proceso y sin técnico. |
| `/agenda-semana` | Agenda de 7 días por técnico y choques de horario. |
| `/folio` | Cómo va un folio y qué le falta. |
| `/nuevo-servicio` | Alta de un mantenimiento, instalación o visita. |
| `/cotizar` | Cotización con partidas e IVA. |
| `/registrar-compra` | Material de un folio o gasto, leyendo el ticket. |
| `/reporte-servicio` | Reporte del servicio a partir de tus notas. |
| `/cobranza` | Quién debe, recordatorios y registro de pagos (administración). |

## Instalar

1. En Claude: Personalización → Plugins → Agregar → Subir plugin → elige `mateclim-service-1.0.0.zip`.
2. Abre el plugin, pestaña **Conectores**, y conecta «mateclim».
3. Inicia sesión con tu cuenta de MateClim y pulsa **Autorizar**. Para registrar, elige consulta y registro.
4. Escribe `/resumen-del-dia`.

Puedes revisar o quitar el acceso cuando quieras en MateClim → Conectar Claude o ChatGPT.

Soporte: matriz@mateclim.com · mateclimservice.com
