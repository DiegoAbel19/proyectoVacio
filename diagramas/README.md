# Diagramas

Todo diagrama del proyecto se dibuja en **draw.io** ([app.diagrams.net](https://app.diagrams.net))
y vive en dos archivos que **deben compartir el mismo nombre base**:

```
diagramas/
├── drawio/          → fuente editable  <nombre>.drawio
└── exportaciones/   → imagen para docs <nombre>.png
```

## Reglas

1. Nomenclatura de archivos: ver `docs/plantillas/plantilla-diagrama-drawio.md`.
2. El `.drawio` **nunca** se borra: es la fuente de verdad.
3. Después de cada modificación, reexportar el PNG (File > Export as > PNG,
   escala 2x para que se lea bien en el informe).
4. Cada documento que usa un diagrama lo referencia con imagen + link al fuente.
5. No subir diagramas de otras herramientas sin avisar.

## Tipos de diagramas del proyecto

| Diagrama | Carpeta de destino en docs/ | Obligatorio |
|----------|------------------------------|-------------|
| Casos de uso | `docs/02-casos-de-uso/` | Sí |
| Clases / dominio | `docs/03-modelo-dominio/` | Sí |
| Secuencia | `docs/04-modelos-interaccion/secuencia/` | según UC |
| Estados | `docs/04-modelos-interaccion/estados/` | si hay ciclo de vida |
| Actividades | `docs/04-modelos-interaccion/actividad/` | opcional |
