# **Texlive+VSCode Configuration in Mac and Win10**

LaTeX is a high-quality typesetting system; it includes features designed for technical and scientific documentation. Latex is the de facto standard for the communication and publication of scientific documents. LaTex is available as [free software](https://www.latex-project.org/lppl/).

## **TeX Live**

[TeX Live](https://www.tug.org/texlive/) is an easy way to get up and running with the TeX document production system. It procides a comprehensive TeX system with binaries for most flavors of Unix, including GNU/Linux, also Windows. It includes all the major TeX-related programs, macro packages, and fonts that are free software, including support for many languages around the world. TeX Live is a integrated environment, including pdflatex, xeletx and so on compilors.The destribution for MacOSX is [MacTex](https://www.tug.org/mactex/).

Downlaod: [TeX Live for Windows](https://www.tug.org/texlive/windows.html), [MacTex distribution](https://www.tug.org/mactex/).

## **Visual Studio Code**

[Visual Studio Code](https://code.visualstudio.com/) is a source code editor developed by Microsoft for Windows, Linux and MacOS. As an outstanding cross-platform eitor, it includes support for debugging, embedded Git control, syntax highlighting, intelligent code completionm snipets, and code refatoring. What's more important, as a open sourced code editing platform, it supports thounds of extensions with extreme extensibility.

Download: [for Windows and MacOS](https://code.visualstudio.com/).

## **LateX Workshop**

[Visual Studio Code LaTex Workshop Extension](https://marketplace.visualstudio.com/items?itemName=James-Yu.latex-workshop) is an extension for Visual Studio Code which is the most crucial step for realizing editing and compiling LaTeX via VSCode. And all the .jason configuration setup will be based on this extension. It has so many practical features such as direct and reverse SyncTex and intellisense. You can find it in [Visual Studio Code Marketplace](https://marketplace.visualstudio.com/items?itemName=James-Yu.latex-workshop) or search it `LaTeX Workshop` in VSCode Extensions keyboard shortcut (`ctrl/cmd`+`P`).

## **Optional Extensions**

[Latex Language Support](https://marketplace.visualstudio.com/items?itemName=torn4dom4n.latex-support) adds syntax highlighting and snippets for LaTex language.

[Latex Preview](https://marketplace.visualstudio.com/items?itemName=ajshort.latex-preview) could realize inline preview of LaTeX documents, automatically updated on save. Even if the VSCode built-in PDF viewer can achieve the same functions......

## **.json Configuration**

1. Using keyboard shortcut (`ctrl/cmd`+`,`) to quick open `Settings`;
2. Add the following .json code into the Settings:

```json
{
    

    "latex-workshop.latex.tools": [
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
          "name": "latexmk",
          "tools": [
            "latexmk"
          ]
        },
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
	        "name": "bibtex",
	        "command": "bibtex",
	        "args": [
	          "%DOCFILE%"
	    	]
        },
        {
	        "name": "pdflatex",
	        "command": "pdflatex",
	        "args": [
	          "-synctex=1",
	          "-interaction=nonstopmode",
	          "-file-line-error",
	          "%DOC%"
	        ]
	    }
    ],
    
    "latex-workshop.latex.recipes": [
        {
            "name": "pdflatex -> bibtex -> pdflatex*2",
            "tools": [
              "pdflatex",
              "bibtex",
              "pdflatex",
              "pdflatex"
            ]
          },
          {
            "name": "latexmk -> bibtex -> xelatex*2",
            "tools": [
              "latexmk",
              "bibtex",
              "xelatex",
              "xelatex"
            ]
          },
        {
          "name": "PDFLaTeX",
          "tools": [
            "pdflatex"
          ]
      	},
        {
          "name": "XeLaTeX",
          "tools": [
            "xelatex"
          ]
        },
        {
          "name": "BibTeX",
          "tools": [
            "bibtex"
          ]
        },
        {
          "name": "xelatex -> bibtex -> xelatex*2",
          "tools": [
            "xelatex",
            "bibtex",
            "xelatex",
            "xelatex"
          ]
        },
        {
          "name": "bibtex -> xelatex",
          "tools": [
          
            "bibtex",
            "xelatex",

          ]
        }
    ],
    


    "latex-workshop.view.pdf.viewer": "browser",
    
    "editor.wordWrap": "on",
    "workbench.colorTheme": "One Dark Pro",
    "workbench.iconTheme": "material-icon-theme",
    "window.zoomLevel": 0
  }
```

3. `ctrl/cmd`+`S` or close with Save.

## Note

Don't forget add TeX Live into `PATH` variables after installation in Windows!
