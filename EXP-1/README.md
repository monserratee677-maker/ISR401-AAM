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
