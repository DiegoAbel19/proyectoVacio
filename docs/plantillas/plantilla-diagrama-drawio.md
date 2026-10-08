# Plantilla — Diagrama draw.io

> Usar este bloque cada vez que un documento (.md) incluya un diagrama.
> Rellenar los campos y eliminar lo que no aplique.

## Cómo se inserta un diagrama en este proyecto

1. **Fuente:** `diagramas/drawio/<nomenclatura>.drawio`
2. **Exporte:** `diagramas/exportaciones/<mismo-nombre>.png`
3. **Referencia desde Markdown:**

```markdown
![Nombre del diagrama](../../diagramas/exportaciones/<mismo-nombre>.png)
*Fuente: [diagrama](../../diagramas/drawio/<nomenclatura>.drawio)*
```

## Nomenclatura de archivos

| Tipo de diagrama | Patrón | Ejemplo |
|------------------|--------|---------|
| Casos de uso | `uc-<id>-<nombre>.drawio` | `uc-01-registrar-pedido.drawio` |
| Secuencia | `seq-<uc>-<nombre>.drawio` | `seq-uc-01-registrar-pedido.drawio` |
| Estados | `est-<objeto>.drawio` | `est-pedido.drawio` |
| Actividades | `act-<nombre>.drawio` | `act-cobrar-pedido.drawio` |
| Clases / dominio | `cls-<nombre>.drawio` | `cls-modelo-dominio.drawio` |

## Bloque para el documento

### Diagrama

![Título del diagrama](../../diagramas/exportaciones/REEMPLAZAR.png)

*Fuente: [REEMPLAZAR.drawio](../../diagramas/drawio/REEMPLAZAR.drawio)*

**Contenido esperado** (qué debe mostrarse, para no perderse al dibujar):

- …
- …

**¿Dónde se dibuja?** [app.diagrams.net](https://app.diagrams.net) → *Extras >
Habilitar el modo UML*, o el plugin/escritorio de draw.io.

## Antes de dar por bueno un diagrama

- [ ] Existe el `.drawio` en `diagramas/drawio/`.
- [ ] Existe el `.png` exportado en `diagramas/exportaciones/` (misma base de nombre).
- [ ] UML correcto para el tipo de diagrama (revisar con la skill `diagramas-drawio`).
- [ ] Nombres de elementos coinciden con glosario y modelo de dominio.
- [ ] La referencia en Markdown carga la imagen y el link al fuente.
