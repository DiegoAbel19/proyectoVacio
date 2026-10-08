---
name: Modelo de dominio
description: Deriva y revisa las entidades del dominio de la Tienda_Automatizada (clases, atributos, relaciones, cardinalidades) a partir de los casos de uso, con trazabilidad y sin entidades sin justificación. Usar cuando se pida armar o revisar el modelo de dominio, el listado de entidades, las relaciones o el diagrama de clases del análisis.
---

# Modelo de dominio

Trabaja sobre `docs/03-modelo-dominio/` usando
`docs/plantillas/plantilla-entidad.md`.

## Flujo de trabajo

1. **Leer** los UC de `docs/02-casos-de-uso/` (y su índice) — la fuente de las
   entidades son los flujos, no la imaginación.
2. **Extraer candidatos:** subrayar sustantivos y objetos de los flujos
   principales y alternativos (pedido, producto, cliente, pago, stock…).
3. **Filtrar** con la prueba: *¿el sistema debe recordar o registrar algo de
   esto?*
   - Sí → entidad.
   - No → descartar (o es dato simple → atributo de otra entidad).
4. Definir por cada entidad: nombre, responsabilidad, atributos mínimos,
   operaciones solo si aportan al análisis.
5. Establecer relaciones y **cardinalidades** derivadas de las reglas de negocio.
6. Escribir el resultado en `01-listado-entidades.md` y `02-relaciones.md`.
7. Dejar el placeholder del diagrama con `docs/plantillas/plantilla-diagrama-drawio.md`
   (nombre de archivo `cls-modelo-dominio.drawio`), o actualizarlo si ya existe.

## Reglas de modelamiento

- **Nombre:** sustantivo en singular, en el lenguaje del dominio del usuario
  (no técnico: «Cliente», no «CustomerDAO»).
- **Sin pensamiento relacional:** nada de tablas, claves primarias ni tipos SQL.
  En análisis se modelan conceptos, no implementación.
- **Atributos vs operaciones:** atributo = dato que se persiste; cálculos y
  reglas van como operaciones o reglas de negocio.
- **Clase o atributo:** si tiene subestructura propia o aparece como objeto en
  varios UC → clase; si es un dato simple de otra → atributo.
- **Trazabilidad bidireccional obligatoria:**
  - entidad → al menos un UC que la use (si no, **borrarla**);
  - UC → al menos las entidades que intervienen en su flujo.
- **Cardinalidades** revisadas contra la regla de negocio real
  («¿puede un pedido tener 0 productos?» → `1..*`).
- **Herencia** solo si hay jerarquía real (ej. Pago ← Tarjeta/Transferencia) y
  simplifica; no usarla por costumbre.
- Si una regla de negocio no está clara para decidir una cardinalidad →
  `[SUPUESTO]` + registrar en `apuntes/dudas-para-clase.md`.

## Antes de dar por terminado

- [ ] Toda entidad trazada a ≥ 1 UC.
- [ ] Sin entidades de relleno ni nombres técnicos.
- [ ] Cada atributo es dato persistido (no un cálculo escondido).
- [ ] Cardinalidades justificadas por regla de negocio.
- [ ] Nombres coinciden con el glosario (`docs/01-requisitos/04-glosario.md`).
- [ ] Placeholder/diagrama `cls-modelo-dominio` referenciado con fuente y PNG.
- [ ] Índice de la carpeta actualizado.
