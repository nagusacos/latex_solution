### build recipes for vscode latex workshop
``` json
"latex-workshop.latex.recipes": [
        {
            "name": "Fast Build (pdflatex)",
            "tools": ["pdflatex"]
        },
        {
            "name": "Quick Build (xelatex)",
            "tools": ["xelatex"]
        },
        {
            "name": "xe->bib->xe*2",
            "tools": ["xelatex", "bibtex", "xelatex", "xelatex"]
        }
    ],
    "latex-workshop.latex.tools": [
        {
            "name": "pdflatex",
            "command": "pdflatex",
            "args": [
                "-synctex=1",
                "-interaction=nonstopmode",
                "-file-line-error",
                "%DOC%"
            ]
        },
        {
            "name": "xelatex",
            "command": "xelatex",
            "args": [
                "-synctex=1",
                "-interaction=nonstopmode",
                "-file-line-error",
                "%DOC%"
            ]
        },
        {
            "name": "bibtex",
            "command": "bibtex",
            "args": ["%DOCFILE%"]
        }
    ],
    "latex-workshop.latex.recipe.default": "Quick Build (xelatex)",
    "latex-workshop.latex.autoBuild.run": "onSave",
    "latex-workshop.latex.autoClean.run": "onBuilt",
    "latex-workshop.view.pdf.viewer": "tab",
    //"workbench.colorTheme": "Dark Modern",
```