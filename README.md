# GA-EXP-02 · Coevaluación de exposiciones

**Asignatura:** ISR-701 Aplicaciones Distribuidas (UTEQ, SPA 2026–2027)
**Estudiante:** Mera Jumbo Allison Michelle
**Fecha de la sesión:** 26 de noviembre de 2026

Informe individual de coevaluación de los equipos expositores (una sección por equipo observado).

## Contenido del repositorio

| Ruta | Qué es |
|------|--------|
| `informe.tex` | Documento principal (carátula, índice y los `\input` de cada equipo) |
| `macros.tex` | Comandos del informe; calcula y escribe la cuenta de la nota sugerida |
| `secciones/equipo_NN.tex` | Una sección por equipo evaluado |
| `secciones/_plantilla_equipo.tex` | Plantilla vacía para agregar equipos |
| `informe.pdf` | PDF compilado del informe |
| `hojas_campo/` | Notas de campo de cada equipo, tomadas en bloc de notas durante la sesión por indicación del docente |
| `sga/entrega_sga.tex` / `.pdf` | PDF de una página que se sube al SGA |

## Cómo compilar

Requisitos: una distribución LaTeX (TeX Live, MiKTeX o Overleaf) con los paquetes
`xfp`, `booktabs`, `longtable`, `hyperref` y `xcolor` (vienen en las instalaciones estándar).

```bash
git clone https://github.com/ameraj2-bit/GA-EXP-02-Coevaluacion.git
cd GA-EXP-02-Coevaluacion

# Informe (se compila dos veces para que salga el índice)
pdflatex informe.tex
pdflatex informe.tex

# PDF de una página para el SGA
cd sga
pdflatex entrega_sga.tex
```

Con `latexmk` también funciona: `latexmk -pdf informe.tex`.

En **Overleaf**: *New Project → Import from GitHub* (o subir el zip), compilador `pdfLaTeX`, documento principal `informe.tex`.

## Nota sugerida

La calcula `\notasugerida{D1}{D2}{D3}{D4}{D5}{D6}` con la fórmula de la guía:

```
NOTA = (10·D1 + 20·D2 + 15·D3 + 20·D4 + 25·D5 + 10·D6) / 4 · 0.1
```

Ejemplo de la guía: niveles 4,3,3,3,4,2 → 325/4 · 0.1 = 8.125 ≈ 8.1.
