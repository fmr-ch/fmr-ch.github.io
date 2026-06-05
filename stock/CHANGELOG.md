# Changelog — App Control de Stock

---

## [1.0.1] — 2026-06-04
### Agregado
- Barra de filtros por categoría en todas las pestañas (Todos, Comida, Limpieza, Higiene, Perro, Casa)
- Cada pestaña mantiene su filtro activo de forma independiente
- Categorías personalizadas: en la pestaña Items, al crear/editar un item se puede agregar una nueva categoría desde el formulario (opción "➕ Nueva categoría...")
- Las categorías nuevas quedan guardadas en localStorage y aparecen automáticamente en los filtros
- Ícono por categoría en filtros y agrupaciones

---

## [1.0.0] — 2026-06-04
### Versión inicial
- Pestaña **Comprar**: KPIs (sin stock / reponer / ok), lista de items a reponer agrupados por categoría con semáforo de estado
- Pestaña **Stock**: vista completa de todos los items con stock actual, objetivo, último precio y fecha de última compra
- Pestaña **Historial**: log de movimientos agrupados por fecha, con tipo (COMPRA/USO), cantidad y precio
- Pestaña **Items**: ABM completo para crear, editar y eliminar items
- Botón **+** flotante para registrar movimientos (compra o uso) con modal
- Al tocar cualquier item se abre el modal con ese item pre-seleccionado
- Registro de compra: cantidad, precio unitario, notas
- Registro de uso: descuenta stock automáticamente
- 38 items pre-cargados de la lista de compras de la dieta semanal (categoría Comida)
- Datos persistidos en `localStorage`
- Categorías base: Comida, Limpieza, Higiene, Perro, Casa
- Compatible con PWA / agregar a pantalla de inicio
