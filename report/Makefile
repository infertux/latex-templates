all: report.pdf

%.pdf: %.tex bibliography.bib glossary.tex
	pdflatex $<
	bibtex $(patsubst %.tex,%.aux,$<)
	makeglossaries $(patsubst %.tex,%.glo,$<)
	pdflatex $<
	pdflatex $<

clean:
	rm report.{aux,bbl,blg,glg,glo,gls,ist,log,out,toc} -f

mrproper: clean
	rm report.pdf -f

.PHONY: clean mrproper all
