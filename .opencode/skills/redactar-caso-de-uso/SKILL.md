---
name: Redactar caso de uso
description: Crea o revisa fichas de casos de uso (UC-XX) del proyecto Tienda_Automatizada siguiendo la plantilla, la nomenclatura y las reglas de trazabilidad de AGENTS.md. Usar cuando se pida crear, completar, mejorar o corregir un caso de uso, o cuando haga falta derivar UC a partir de requisitos.
---

# Redactar caso de uso

Genera una ficha UC válida para `docs/02-casos-de-uso/`.
Antes de escribir, revisar `AGENTS.md` secciones 2, 4 y el checklist de
`docs/02-casos-de-uso/README.md`.

## Flujo de trabajo

1. **Recopilar contexto** (leer si existen):
   - `docs/01-requisitos/01-actores-y-alcance.md` → actores válidos.
   - `docs/01-requisitos/02-requisitos-funcionales.md` → RF que debe cubrir.
   - `docs/02-casos-de-uso/00-indice-casos-de-uso.md` → numeración siguiente libre.
2. **Preguntar lo que falte** (regla 3 de AGENTS.md): actor principal, meta real,
   reglas de negocio involucradas. No inventar el flujo si no se conoce.
3. **Copiar** `docs/plantillas/plantilla-caso-de-uso.md` como base.
4. Redactar la ficha aplicando las reglas de la sección «Reglas».
5. **Actualizar el índice** `00-indice-casos-de-uso.md` con el nuevo UC.
6. Verificar el checklist final y ofrecerlo al usuario.

## Reglas de redacción

- **Nombre:** verbo en infinitivo + objeto («Registrar pedido», «Consultar stock»).
  Nunca: «Hacer clic en…», «Pantalla de…», «Uso de…».
- **Nivel meta-usuario:** el actor debe poder decir «con esto logré mi objetivo»
  al final del flujo principal.
- **Actor principal** = quien tiene la meta. **Secundario** = quien auxilia
  (puede ser otro sistema).
- **Precondiciones:** solo las que dependen del mundo del sistema, no del
  comportamiento del actor (ej. «El cliente está autenticado» sí; «El usuario
  tiene ganas de comprar» no).
- **Flujo principal:** 4–9 pasos numerados, alternando acción del actor /
  respuesta del sistema. Termina cumpliendo la meta.
- **Alternativos:** cada uno con su **condición de entrada** y el paso al que
  vuelve. **Excepciones:** errores del sistema o datos inválidos → terminan sin
  cumplir la meta.
- **Reglas de negocio** explícitas (BR-XX) si el flujo depende de una.
- **Trazabilidad:** listar los RF-XX que cubre; si un RF queda sin UC, avisar.

## Antes de dar por buena la ficha

- [ ] El nombre es de nivel meta-usuario (sin UI ni tecnología).
- [ ] El flujo principal cumple la meta del actor.
- [ ] Cada alternativo/excepción tiene condición concreta.
- [ ] Precondiciones y postcondiciones presentes (éxito y fallo).
- [ ] RF relacionados listados; índice actualizado.
- [ ] Nomenclatura `UC-XX` con el número siguiente libre.
- [ ] Diagrama: insertar con `docs/plantillas/plantilla-diagrama-drawio.md`
      (o dejar placeholder con instrucciones — nunca dar por existente un
      diagrama que no está en `diagramas/`).

## Si el usuario está practicando

Si el usuario pide «haceme el UC de X» estando en modo práctica, aplicar el
bloque D de la skill `tutor-modelamiento`: dar criterios + su esquema corregido,
no la ficha completa resuelta.
