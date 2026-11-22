# EXP-1 · GA-SUM-02

Exposición sobre herramientas automatizadas de gestión de requisitos (Jira), aplicada al caso UteqFit-AI.
Grupo AAM · ISR-401 · UTEQ.

## Estructura

```
EXP-1/
├── README.md         Este archivo
├── main.tex          Diapositivas (Beamer)
├── referencias.bib   Referencias IEEE
├── main.pdf          PDF compilado
├── figuras/          Capturas y figuras propias
└── evidencias/       Exportación de Jira (CSV) y otras evidencias
```

## Compilación

- Compilador: pdfLaTeX
- Archivo principal: `main.tex`
- Distribución probada: TeX Live 2024 (o MiKTeX actualizado)
- Paquetes: beamer, babel (spanish), graphicx, booktabs, tabularx, xcolor, tikz, lmodern
- Estilo bibliográfico: `IEEEtran.bst` (paquete `ieeetran` de TeX Live)

Opción 1 (automática), desde esta carpeta:

```
latexmk -pdf main.tex
```

Opción 2 (manual, en este orden), desde esta carpeta:

```
pdflatex main.tex
bibtex main
pdflatex main.tex
pdflatex main.tex
```

## Demostración en Jira (diapositivas 7 a 9)

Caso de práctica: UteqFit-AI, sistema para el Gimnasio Universitario (UBU) de la UTEQ.

- Espacio: **UteqFit-AI** (clave `UTEQFIT`), plantilla Scrum, plan gratuito de Jira Cloud.
- Épicas por módulo del sistema; historias de usuario con etiqueta `RF` o `RNF`.
- Campos de cada historia: ID del requisito, prioridad MoSCoW, fuente (técnica de elicitación y fecha) y criterio de aceptación.
- Capturas en `figuras/`: `tablero.png`, `requisito.png` y `flujo.png`.
- Exportación CSV de los requisitos en `evidencias/jira_export.csv`.

### Flujo de trabajo de los requisitos

```
Propuesto → En análisis → Validado → Aprobado
                 ↑            │
                 └─rechazado──┘
```

Filtro JQL de ejemplo: `project = UTEQFIT AND labels = RF AND status = Aprobado`
