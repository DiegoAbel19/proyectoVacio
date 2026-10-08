# Diagrama de clases — modelo de dominio

> Diagrama con la fuente en `diagramas/drawio/cls-modelo-dominio.drawio`.
> Ver `docs/plantillas/plantilla-diagrama-drawio.md` para el bloque de inserción.

## Diagrama

*(Pendiente — placeholder para el diagrama de clases del dominio.)*

```markdown
![Modelo de dominio](../../diagramas/exportaciones/cls-modelo-dominio.png)
*Fuente: [cls-modelo-dominio.drawio](../../diagramas/drawio/cls-modelo-dominio.drawio)*
```

## Qué debe mostrar

- Entidades de `01-listado-entidades.md` con sus atributos clave.
- Asociaciones y cardinalidades de `02-relaciones.md`.
- Herencia solo si existe en el dominio.

## Instrucciones de dibujo (draw.io)

1. Abrir [app.diagrams.net](https://app.diagrams.net) → *Extras → Habilitar…* → librería **UML**.
2. Crear un rectángulo de clase por entidad (secciones: nombre / atributos / operaciones).
3. Unir con asociaciones y anotar cardinalidades (`1`, `0..*`, `1..*`).
4. Guardar como `diagramas/drawio/cls-modelo-dominio.drawio` y exportar PNG 2x
   a `diagramas/exportaciones/`.
