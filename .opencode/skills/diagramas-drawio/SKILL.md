---
name: Diagramas draw.io
description: Diseña, revisa y exporta diagramas UML del proyecto Tienda_Automatizada en draw.io (casos de uso, secuencia, estados, actividades, clases) aplicando la nomenclatura de archivos, las convenciones de dibujo y el proceso de exportación PNG. Usar cuando se pida crear o corregir un diagrama, exportarlo, o insertarlo en un documento Markdown.
---

# Diagramas draw.io

El proyecto dibuja en **draw.io / app.diagrams.net**. Los diagramas no se
generan como código: se **describen** para que el usuario los dibuje, o se
revisan. Nomenclatura y bloque de inserción: `docs/plantillas/plantilla-diagrama-drawio.md`.

## Flujo de trabajo

1. **Identificar el tipo** de diagrama y su UC/entidad de referencia.
2. **Verificar nomenclatura** del archivo:
   `uc-<id>-…`, `seq-<uc>-…`, `est-<objeto>`, `act-…`, `cls-…` (ver plantilla).
3. **Preparar el contenido** del diagrama (qué elementos van) — punto 4 abajo.
4. **Entregar instrucciones de dibujo** al usuario:
   - pasos concretos: «Crearía 5 actores/titulares…, 4 casos de uso…, incluir
     `<<include>>`/`<<extend>>` entre…»;
   - dónde habilitar UML en draw.io: *Extras → Habilitar…* (o `?splash=0`,
     panel de librerías → UML);
   - qué NO dibujar (evitar ruido).
5. **Exportar:** File → Export as → PNG, escala **2x**, en
   `diagramas/exportaciones/<mismo-nombre>.png`; fuente en `diagramas/drawio/`.
6. **Insertar** en el Markdown con la plantilla (imagen + link al `.drawio`).
7. Si el diagrama aún no existe en el repo, dejar **placeholder + instrucciones**
   (regla AGENTS.md §4): nunca afirmar que un diagrama existe sin verificarlo.

## Qué debe contener cada tipo

| Tipo | Elementos mínimos | Errores comunes |
|------|-------------------|-----------------|
| **Casos de uso** | Actores (silueta), frontera del sistema, elipses con nombre V+obj, `<<include>>`/`<<extend>>` con dirección correcta, relaciones actor–UC | Poner UC de interfaz; `<<extend>>` invertido; actores duplicados |
| **Secuencia** | Lifelines de actor y objetos, mensajes numerados en orden, barras de activación, devolución punteada, marcas de inicio/fin | Mensajes sin orden; objetos que no son del modelo de dominio; saltos de tiempo sin indicar |
| **Estados** | Estado inicial (punto), fin (diana), estados redondeados, transiciones con `evento [condición] / acción`, estado final | Transiciones sin condición; estados que son acciones |
| **Actividades** | Nodo inicial/final, acciones, rombo de decisión con etiquetas, barras de fork/join,泳 lanes si hay varios actores | Decisión sin etiquetas; mezclar con diagrama de flujo de código |
| **Clases** | Rectángulo en 3 secciones (nombre/atributos/operaciones), asociaciones con cardinalidades 1/0..*/1..*, `<<include>>` no aplica, agregación/composición cuando corresponda | Tipos SQL; nombres técnicos; cardinalidades inventadas |

**Sobre `<<include>>` vs `<<extend>>`:**
- `include` = comportamiento **obligatorio y común** extraído (flecha A→B, «B siempre pasa»).
- `extend` = comportamiento **opcional** que se agrega bajo condición (flecha
  B→A con `<<extend>>` apuntando al caso base, «solo si…»).
Si no se puede justificar la condición → mejor no usar `<<extend>>`.

## Checklist de calidad (antes de exportar)

- [ ] UML correcto para el tipo (ver tabla).
- [ ] Nombres de elementos iguales a glosario, UC y modelo de dominio.
- [ ] Sin texto de UI ni de tecnología.
- [ ] Diagrama legible: sin cruces de flechas innecesarios, tamaños uniformes.
- [ ] Archivo `.drawio` guardado en `diagramas/drawio/`.
- [ ] PNG 2x exportado en `diagramas/exportaciones/` con el mismo nombre base.
- [ ] Referencia insertada en el documento (imagen + link).
- [ ] Diagrama relacionado con el documento correcto (trazabilidad UC ↔ diagrama).
