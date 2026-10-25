# MateClim Service para Claude

Plugins oficiales de [MateClim Service](https://mateclimservice.com) para Claude. Con ellos, Claude se conecta a tu cuenta de MateClim y te ayuda con el trabajo diario de tu empresa de aire acondicionado y refrigeración.

Claude entra con tu usuario y solo puede ver y hacer lo que tu rol permite. Antes de guardar cualquier cosa te muestra lo que va a registrar y espera tu «sí».

## Plugin: MateClim Service

| Comando | Qué hace |
| --- | --- |
| `/resumen-del-dia` | Trabajos de hoy, atrasados, en proceso y sin técnico. |
| `/agenda-semana` | Agenda de 7 días por técnico y choques de horario. |
| `/folio` | Cómo va un folio y qué le falta. |
| `/nuevo-servicio` | Alta de un mantenimiento, instalación o visita. |
| `/cotizar` | Cotización con partidas e IVA. |
| `/registrar-compra` | Material de un folio o gasto, leyendo el ticket o la factura. |
| `/reporte-servicio` | Reporte del servicio a partir de tus notas. |
| `/cobranza` | Quién debe, recordatorios y registro de pagos (administración). |

También puedes pedirlo con tus palabras: «¿qué tiene Juan mañana?», «agenda un mantenimiento para el lunes a las 10», «¿ya pagó el cliente del folio ABC-MNT-0012?».

## Instalar en Claude (web, escritorio o celular)

1. Abre Claude → **Personalización** → **Plugins**.
2. Pulsa **Agregar** → **Agregar marketplace** y escribe `MateClimService/mateclim-plugins`.
3. Instala **MateClim Service**.
4. En el plugin, abre la pestaña **Conectores** y conecta «mateclim».
5. Inicia sesión con tu cuenta de MateClim y pulsa **Autorizar** (elige consulta y registro si quieres que Claude registre por ti).
6. Escribe `/resumen-del-dia`.

Las nuevas versiones del plugin llegan desde este marketplace; no tienes que volver a instalar nada.

## Instalar en Claude Code

```
/plugin marketplace add MateClimService/mateclim-plugins
/plugin install mateclim-service@mateclim
```

## Privacidad y acceso

- No necesitas claves ni contraseñas en Claude: la conexión se autoriza en MateClim con tu sesión.
- Puedes ver y quitar el acceso cuando quieras en MateClim → **Conectar Claude o ChatGPT**.
- Lo que consultes pasa también por tu cuenta de Claude y se rige por sus condiciones.

## Soporte

matriz@mateclim.com · [mateclimservice.com](https://mateclimservice.com)

---

### Para el equipo de MateClim: publicar una actualización

1. Cambia lo necesario en `plugins/mateclim-service/`.
2. Sube `version` en `plugins/mateclim-service/.claude-plugin/plugin.json` (por ejemplo, de 1.0.0 a 1.0.1). Sin ese cambio los clientes se quedan en la versión anterior.
3. Valida con `claude plugin validate . --strict`.
4. Haz commit y push a `main`.
