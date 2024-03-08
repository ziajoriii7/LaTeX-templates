
DOC = <.tex-filename-no-extension>

LATEX = lualatex
LATEX_OPTS = -shell-escape

all: $(DOC).pdf

$(DOC).pdf: $(DOC).tex
	$(LATEX) $(LATEX_OPTS) $(DOC)

clean:
	psh -c "Remove-Item -Force $(DOC).* -Include *.aux, *.log, *.out, *.toc -ErrorAction SilentlyContinue"
	pwsh -c "Remove-Item -Force $(DOC)-plantuml.* -ErrorAction SilentlyContinue"
	pwsh -c "Remove-Item -Force $(DOC).pytxcode -ErrorAction SilentlyContinue"

cleanall: clean
	pwsh -c "Remove-Item -Force $(DOC).pdf -ErrorAction SilentlyContinue"

.PHONY: all clean cleanall
