# Set the environment variables for the paper and bibtex name
FILE=workflow
BIB=workflow.bib

# This gets called when you type 'make'
all: pdf

# Sequence of commands based on latex (try if 'pdf' does not work)
doc: ${FILE}.tex ${BIB}
	latex ${FILE}.tex
	latex ${FILE}.tex
	bibtex ${FILE}
	latex ${FILE}.tex
	latex ${FILE}.tex
	dvips ${FILE}.tex
	ps2pdf ${FILE}.tex

# Sequence of commands based on pdflatex
pdf: ${FILE}.tex ${BIB}
	pdflatex ${FILE}.tex
	pdflatex ${FILE}.tex
	bibtex ${FILE}
	pdflatex ${FILE}.tex
	pdflatex ${FILE}.tex

# Remove temporary files (helps when things are not refreshing)
clean:
	rm -f *.aux *.blg *.dvi *.log *.ps *.bbl *.out *.spl
