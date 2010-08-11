BIBTEX=bibtex
LATEX=latex
PDFLATEX=pdflatex
DVIPSPDF=dvips -Ppdf
PS2PDF=ps2pdf
TOEPS=mogrify -format eps


all: msc-report

msc-report: msc-report.tex
	$(TOEPS) gfx/*/*.png
	$(LATEX) $@
	$(DVIPSPDF) $@
	$(BIBTEX) $@
	$(LATEX) $@
	$(DVIPSPDF) $@
	$(LATEX) $@
	$(DVIPSPDF) $@
	$(PS2PDF) msc-report.ps msc-report.pdf

clean:
	-rm -rf *.pdf *.ps *.dvi *.aux *.log *.bbl *.blg *.lof *.lot *.toc *~
	-rm -rf gfx/*/*.eps
