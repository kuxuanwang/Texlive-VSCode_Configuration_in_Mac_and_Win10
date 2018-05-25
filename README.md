# Texlive+VSCode Configuration in Mac and Win10

LaTeX is a high-quality typesetting system; it includes features designed for technical and scientific documentation. Latex is the de facto standard for the communication and publication of scientific documents. LaTex is available as [free software](https://www.latex-project.org/lppl/).

## TeX Live

[TeX Live](https://www.tug.org/texlive/) is an easy way to get up and running with the TeX document production system. It procides a comprehensive TeX system with binaries for most flavors of Unix, including GNU/Linux, also Windows. It includes all the major TeX-related programs, macro packages, and fonts that are free software, including support for many languages around the world. TeX Live is a integrated environment, including pdflatex, xeletx and so on compilors.The destribution for MacOSX is [MacTex](https://www.tug.org/mactex/).

Downlaod: [TeX Live for Windows](https://www.tug.org/texlive/windows.html), [MacTex distribution](https://www.tug.org/mactex/).

## Visual Studio Code

[Visual Studio Code](https://code.visualstudio.com/) is a source code editor developed by Microsoft for Windows, Linux and MacOS. As an outstanding cross-platform eitor, it includes support for debugging, embedded Git control, syntax highlighting, intelligent code completionm snipets, and code refatoring. What's more important, as a open sourced code editing platform, it supports thounds of extensions with extreme extensibility.

Download: [for Windows and MacOS](https://code.visualstudio.com/).

```json
{
    "latex-workshop.view.pdf.viewer": "tab",
    "latex-workshop.latex.recipes": [
        {
          "name": "latexmk -> bibtex -> xelatex*2",
          "tools": [
            "latexmk",
            "bibtex",
            "xelatex",
            "xelatex"
          ]
        }
    ],
    "latex-workshop.latex.clean.enabled": true,

    "latex-workshop.latex.clean.fileTypes": [
      "*.aux",
      "*.bbl",
      "*.blg",
      "*.idx",
      "*.ind",
      "*.lof",
      "*.lot",
      "*.out",
      "*.toc",
      "*.acn",
      "*.acr",
      "*.alg",
      "*.glg",
      "*.glo",
      "*.gls",
      "*.ist",
      "*.fls",
      "*.log",
      "*.fdb_latexmk",
    ],
  }
  ```
