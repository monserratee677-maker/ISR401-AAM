# EXP-1 · GA-SUM-02

Exposición sobre herramientas automatizadas para gestionar requisitos, aplicada al caso UteqFit-AI.

## Archivos

- `main.tex`: presentación Beamer.
- `referencias.bib`: fuentes citadas en estilo IEEE.
- `main.pdf`: PDF compilado.
- `compilar.py`: script de compilación con Tectonic.
- `figuras/`: capturas y figuras.
- `evidencias/`: exportaciones de Jira y otros respaldos.

## Requisitos

- Python 3.8 o posterior.
- Tectonic. El script lo busca en el `PATH` y en la carpeta habitual de instalación de Windows. Si no lo encuentra, ofrece instalar el ejecutable oficial y agregarlo al `PATH` del usuario. Después de instalarlo, las siguientes ejecuciones compilan directamente.

## Compilar

Abre una terminal en esta carpeta y ejecuta:

```powershell
python .\compilar.py
```

También puedes usar `py .\compilar.py` si ese es el comando configurado en tu equipo. El script compila `main.tex`, resuelve las referencias y deja el PDF final en `main.pdf`; los archivos intermedios quedan en `build/`.

Para ejecutar Tectonic directamente:

```powershell
tectonic --outdir build main.tex
```

La primera compilación necesita conexión a Internet para descargar los recursos de LaTeX que todavía no estén en caché.

## Demostración en Jira (diapositivas 7 a 9)

El caso es UteqFit-AI, un sistema para el Gimnasio Universitario (UBU) de la UTEQ. El espacio usa plantilla Scrum; sus épicas representan módulos y las historias se clasifican como `RF` o `RNF`. Cada historia registra el ID, prioridad MoSCoW, fuente y criterio de aceptación.

Las capturas del tablero, el requisito `REQ-001` y el flujo se guardan en `figuras/`. La exportación de Jira se encuentra en `evidencias/jira_export.csv`.

El flujo configurado es:

```text
Propuesto → En análisis → Validado → Aprobado
                 ↑            │
                 └─rechazado──┘
```

Filtro JQL de ejemplo: `project = UTEQFIT AND labels = RF AND status = Aprobado`.
