.PHONY: all clean

all: diploma.pdf annotation.pdf

diploma.aux: diploma.tex
	pdflatex $<
	rm -f diploma.pdf

diploma.pdf: diploma.tex title.tex diploma.aux
	bibtex diploma.aux
	pdflatex $<
	pdflatex $<

annotation.pdf: annotation.tex
	pdflatex $<

clean:
	rm -f *.{toc,aux,log,pdf} diploma.bbl diploma.blg
