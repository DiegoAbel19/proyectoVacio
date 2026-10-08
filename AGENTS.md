# AGENTS.md — Reglas del proyecto Tienda_Automatizada

Este archivo define cómo debe trabajar cualquier agente de IA en este repositorio.
Léelo completo antes de crear o modificar archivos.

---

## 1. Contexto

- **Materia:** Análisis y Modelamiento de Software.
- **Alcance:** documentación de análisis + modelos UML (draw.io).
  **No se escribe código de la aplicación** (Java, Python, SQL, etc.) salvo
  petición explícita del usuario en el momento.
- **Usuario:** estudiante en proceso de aprendizaje. Las respuestas deben ser
  didácticas: explicar el *por qué*, no solo entregar el resultado.
- **Idioma:** español en todo el contenido (archivos, diagramas, commits).

---

## 2. Reglas generales

1. **Explicar antes de producir.** Cuando se pida un documento o diagrama, primero
   2–4 líneas de contexto: qué es, para qué sirve en el proyecto y qué decisión
   falta. Después generar.
2. **Marcar supuestos.** Toda información que no venga del usuario se marca como
   `[SUPUESTO]` en el propio documento, para revisión.
3. **No inventar decisiones.** Si falta un dato clave (actor, regla de negocio,
   alcance), **preguntar** antes de rellenar. Preferible una pregunta corta a un
   documento relleno con inventos.
4. **No borrar trabajo del usuario.** Antes de sobrescribir un archivo que ya tiene
   contenido propio, mostrar el cambio o preguntar.
5. **Usar las plantillas** de `docs/plantillas/` como punto de partida de cada
   documento. No inventar formatos nuevos salvo que la plantilla no exista.
6. **Mantener los índices.** Todo documento nuevo debe quedar referenciado en el
   índice o README de su carpeta.
7. **Markdown limpio:** un H1 por archivo, tablas para listados de requisitos/UC,
   rutas relativas en los links.
8. **No dejar carpetas vacías:** cada carpeta lleva al menos un `README.md` que
   explique qué va ahí.

---

## 3. Dónde va cada cosa

| Contenido | Ruta |
|-----------|------|
| Alcance, actores, RF, RNF, glosario | `docs/01-requisitos/` |
| Fichas de casos de uso e índice UC | `docs/02-casos-de-uso/` |
| Entidades del dominio y relaciones | `docs/03-modelo-dominio/` |
| Diagramas de secuencia / estados / actividad | `docs/04-modelos-interaccion/` |
| Informes y entregas | `docs/05-entregables/` |
| Plantillas para copiar | `docs/plantillas/` |
| Fuentes `.drawio` | `diagramas/drawio/` |
| Exportes PNG/SVG | `diagramas/exportaciones/` |
| Conceptos aprendidos / dudas de clase | `apuntes/` |
| Bibliografía y enlaces | `recursos/` |
| Skills del proyecto | `.opencode/skills/` |

**Nunca** crear documentos de análisis fuera de `docs/` ni `.drawio` fuera de
`diagramas/drawio/`.

---

## 4. Reglas de modelamiento

- **Nomenclatura fija:** `RF-XX`, `RNF-XX`, `UC-XX`. Numéricos de 2 dígitos y
  correlativos; no reutilizar números borrados.
- **Caso de uso:** nombre = *verbo en infinitivo + objeto* («Registrar pedido»),
  nivel de meta-usuario, **sin** detalles de interfaz ni de tecnología.
  Flujo principal en pasos numerados; alternativos y de excepción con su condición.
- **Requisito:** verificable y sin ambigüedad (evitar «rápido», «fácil», «etc.»).
  Si es medible, indicar la métrica.
- **Trazabilidad obligatoria:**
  - cada `RF` asociado a ≥ 1 `UC`;
  - cada `UC` referenciado en las entidades que usa;
  - cada entidad justificada por al menos un `UC`.
  Si algo no se puede trazar, señalarlo en vez de forzar la relación.
- **Diagramas draw.io:**
  1. fuente en `diagramas/drawio/<nomenclatura>.drawio`;
  2. exporte PNG en `diagramas/exportaciones/<mismo-nombre>.png`;
  3. el documento que lo usa lo referencia con imagen + link al fuente
     (usar `docs/plantillas/plantilla-diagrama-drawio.md`);
  4. si el diagrama aún no existe, dejar el placeholder con instrucciones de dibujo
     — **nunca** dar por existente un diagrama que no está en el repo.
- **Dudas de modelamiento** (¿es clase o atributo?, ¿cuántos actores?, etc.):
  resolver con explicación + opción recomendada, y registrar en
  `apuntes/dudas-para-clase.md` si sigue abierta.

---

## 5. Aprendizaje (prioridad alta)

- Si el usuario pregunta **qué es / para qué sirve / cómo se hace** un concepto de
  la materia → usar la skill `tutor-modelamiento`.
- Si el usuario está **practicando** (pide resolver un ejercicio, corregir su
  respuesta): **guiar en vez de resolver**. Dar pistas, criterios de corrección y
  recién después, si lo pide, la solución comentada.
- Al terminar de generar un documento, ofrecer el **checklist de la fase** para que
  el usuario verifique qué falta.
- Sugerir (no forzar) pasar lo nuevo a `apuntes/conceptos.md` con palabras propias.

---

## 6. Skills disponibles

| ID | Usar cuando… |
|----|----------------|
| `tutor-modelamiento` | Se explique un concepto de la materia o se pida practicar |
| `redactar-caso-de-uso` | Se cree o revise una ficha UC-XX |
| `revisar-requisitos` | Se agreguen o auditen RF/RNF |
| `modelo-dominio` | Se derive o revise el modelo de entidades |
| `diagramas-drawio` | Se diseñe, revise o exporte un diagrama UML |

---

## 7. Git

- Commits en **español**, formato `<tipo>: <descripción breve>`, tipos:
  `docs`, `modelos`, `plantillas`, `skills`, `repo`.
- Un commit por unidad de cambio coherente.
- **Confirmar con el usuario antes de hacer commit o push.**
- No hacer `reset`, `revert` ni borrar historial sin pedirlo explícitamente.

---

## 8. Checklist antes de dar por terminada una tarea

- [ ] El archivo quedó en la carpeta correcta (sección 3).
- [ ] Se usó la plantilla correspondiente.
- [ ] Índice/README de la carpeta actualizado.
- [ ] Supuestos marcados con `[SUPUESTO]`.
- [ ] Trazabilidad RF ↔ UC ↔ entidades verificada.
- [ ] Diagramas referenciados con fuente `.drawio` y exporte `.png`.
- [ ] Contenido en español.
