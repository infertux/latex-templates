all: paper.pdf

%.pdf: %.tex bibliography.bib
	pdflatex $<
	bibtex $(patsubst %.tex,%.aux,$<)
	pdflatex $<
	pdflatex $<

clean:
	rm paper.{aux,log,bbl,blg,out} -f

mrproper: clean
	rm paper.pdf -f

.PHONY: clean mrproper all
