all: essay.pdf

%.pdf: %.tex bibliography.bib
	pdflatex $<
	bibtex $(patsubst %.tex,%.aux,$<)
	pdflatex $<
	pdflatex $<

clean:
	rm essay.{aux,bbl,blg,log,out,toc} -f

mrproper: clean
	rm essay.pdf -f

.PHONY: clean mrproper all
