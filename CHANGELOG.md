# Changelog — App Análisis de Presupuesto

---

## [1.0.6] — 2026-06-04
### Correcciones
- Bug en cálculo de `daysSince`: usaba hora actual en vez de medianoche, causando que el primer día del período mostrara presupuesto de 2 días en DISPONIBLE
### Agregado
- Segunda fila de estadísticas (azul) con datos del bloque actual: por día del bloque, gastado en bloque, días restantes del bloque
- Card "Período actual" debajo de Bloque actual: muestra presupuesto total del período, gastado total y disponible (verde/rojo)

---

## [1.0.5] — 2026-06-04
### Correcciones
- "Por día" ahora calcula `(presupuesto libre total − gastos acumulados) / (días restantes + 1)`
- "Días restantes" excluye el día actual (está en curso); "Por día" suma +1 para incluirlo como día de gasto activo

---

## [1.0.4] — 2026-06-04
### Cambios
- Campo "Fecha fin" renombrado a "Próximo sueldo"; el sistema calcula automáticamente `endDate = nextPayday - 1 día`
- "Disponible acumulado" renombrado a "Disponible"
- "Por día" ahora muestra disponible restante ÷ días restantes (dinámico)
- "Días restantes" excluye el día actual
- Chips de bloque ahora son seleccionables; al tocar un bloque muestra su saldo acumulado (presupuesto + carryover − gastos hasta ese punto)
- `selectedBlock` se resetea al cambiar de período activo

---

## [1.0.3] — 2026-06-04
### Cambios
- Cuestionario de 6 pasos reemplazado por formulario de un único paso
- Campos: Mes (desplegable), Año (año actual y siguiente únicamente), Presupuesto (manual), Fecha inicio (calendario mes actual), Fecha fin (calendario mes siguiente)
- Botón Guardar se habilita solo cuando todos los campos están completos

---

## [1.0.2] — 2026-06-04
### Agregado
- Pestaña "Períodos" con listado de períodos cargados
- Cuestionario de 6 pasos para crear un nuevo período: mes → año → presupuesto libre → fecha inicio → fecha fin → confirmación con resumen
- Soporte para múltiples períodos; el período activo se selecciona tocando cualquier ítem de la lista
- Auto-selección del período activo según la fecha actual
- Migración automática de configuración legacy (settings anteriores)
- `selectedBlock` se resetea al cambiar período

---

## [1.0.1] — 2026-06-04
### Correcciones
- Fix en cálculo de días totales del período: `daysBetween` ahora suma +1 para incluir ambos extremos (inicio y fin), corrigiendo presupuesto diario de $16.774 a $16.250

---

## [1.0.0] — 2026-06-04
### Versión inicial
- Pestaña **Hoy**: disponible acumulado con barra de progreso, estadísticas (por día, hoy gastado, días restantes), info de bloque actual, gastos del día
- Pestaña **Historial**: gastos agrupados por fecha
- Pestaña **Análisis**: gasto por categoría con barras, totales del período
- Pestaña **Config**: borrar gastos, borrar períodos
- Modal de carga de gasto: monto, concepto, categoría (comida, gusto, limpieza, casa, perro)
- Botón flotante "+" para acceso rápido
- Datos persistidos en `localStorage`
- Compatible con PWA / agregar a pantalla de inicio
- Configuración inicial: período junio 2026 (04/06 → 05/07), libre $520.000
