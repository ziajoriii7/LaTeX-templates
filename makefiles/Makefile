DOC = <.tex-filename-no-extension>

LATEX = lualatex
LATEX_OPTS = -shell-escape

all: $(DOC).pdf

$(DOC).pdf: $(DOC).tex
	$(LATEX) $(LATEX_OPTS) $(DOC)

clean:
	del /Q /F $(DOC).aux $(DOC).log $(DOC).out $(DOC).toc
	del /Q /F $(DOC)-plantuml.*
	del /Q /F $(DOC).pytxcode

cleanall: clean
	del /Q /F $(DOC).pdf

.PHONY: all clean cleanall

