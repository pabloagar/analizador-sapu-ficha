# Analizador Institucional SAPU

Una guardia puede empezar un mes y terminar el siguiente. Para revisar las horas de un Servicio de Atención Primaria de Urgencia (SAPU), desarrollé una herramienta que abre los reportes en el navegador, separa los tramos de cada turno y permite revisar de dónde sale el total. Funciona sin conexión y genera archivos de respaldo e informes.

## Un turno entre dos meses

Ejemplo ficticio de una guardia entre el martes 31 de marzo y el miércoles 1 de abril de 2026. En el ejemplo, ambos días son hábiles y el turno va de 21:00 a 03:00.

| Período seleccionado | Tramo asignado | Horas que aporta al período |
|---|---|---:|
| Marzo | 31 de marzo, de 21:00 a medianoche | 3 |
| Abril | 1 de abril, de medianoche a 03:00 | 3 |

La persona que revisa el mes puede comprobar los tramos antes de descargar el detalle en CSV. La herramienta acumula los minutos por mes y tarifa antes de calcular las horas completas. También permite generar planillas e informes Word según el flujo seleccionado.

## Qué se probó

La validación técnica de la versión 18, documentada el 1 de noviembre de 2026, cubrió 17 casos del motor de horas, incluidos cambios de mes, feriados, turnos duplicados y solapamientos. Con reportes sintéticos también se comprobó en Edge la lectura de PDF y la generación de archivos sin conexión. Queda pendiente contrastar un período autorizado con los totales que utiliza la institución.

**Desarrollo:** Pablo Aguirre Araya, médico general de zona en Arica, Chile.
