pdf	: thesis1.pdf \
	  thesis2.pdf \
	  thesis3.pdf \
	  thesis4.pdf \
	  thesis5.pdf \
	  thesis6.pdf \
	  thesis7.pdf \
	  thesis8.pdf \
	  thesis9.pdf \
	  thesis10.pdf

ps	: thesis1.ps \
	  thesis2.ps \
	  thesis3.ps \
	  thesis4.ps \
	  thesis5.ps \
	  thesis6.ps \
	  thesis7.ps \
	  thesis8.ps \
	  thesis9.ps \
	  thesis10.ps

thesis1.ps	: thesis1.dvi
		dvips -o thesis1.ps thesis1

thesis1.dvi	: thesis1.tex
		latex thesis1
		latex thesis1

thesis1.pdf	: thesis1.tex
		pdflatex thesis1
		pdflatex thesis1

thesis2.ps	: thesis2.dvi
		dvips -o thesis2.ps thesis2

thesis2.dvi	: thesis2.tex \
		  intro.tex techintro.tex method.tex results.tex conc.tex
		latex thesis2
		latex thesis2

thesis2.pdf	: thesis2.tex \
		  intro.tex techintro.tex method.tex results.tex conc.tex
		pdflatex thesis2
		pdflatex thesis2

thesis3.ps	: thesis3.dvi
		dvips -o thesis3.ps thesis3

thesis3.dvi	: thesis3.tex mythesis.cls
		latex thesis3
		latex thesis3

thesis3.pdf	: thesis3.tex mythesis.cls
		pdflatex thesis3
		pdflatex thesis3

thesis4.ps	: thesis4.dvi
		dvips -o thesis4.ps thesis4

thesis4.dvi	: thesis4.tex thesis.bib
		latex thesis4
		bibtex thesis4
		latex thesis4
		latex thesis4

thesis4.pdf	: thesis4.tex thesis.bib
		pdflatex thesis4
		bibtex thesis4
		pdflatex thesis4
		pdflatex thesis4

thesis5.ps	: thesis5.dvi
		dvips -o thesis5.ps thesis5

thesis5.dvi	: thesis5.tex thesis.bib
		latex thesis5
		bibtex thesis5
		latex thesis5
		latex thesis5

thesis5.pdf	: thesis5.tex thesis.bib
		pdflatex thesis5
		bibtex thesis5
		pdflatex thesis5
		pdflatex thesis5

thesis6.ps	: thesis6.dvi
		dvips -o thesis6.ps thesis6

thesis6.dvi	: thesis6.tex thesis.bib
		latex thesis6
		bibtex thesis6
		latex thesis6
		latex thesis6

thesis6.pdf	: thesis6.tex thesis.bib
		pdflatex thesis6
		bibtex thesis6
		pdflatex thesis6
		pdflatex thesis6

thesis7.ps	: thesis7.dvi
		dvips -o thesis7.ps thesis7

thesis7.dvi	: thesis7.tex thesis.bib
		latex thesis7
		bibtex thesis7
		latex thesis7
		latex thesis7

thesis7.pdf	: thesis7.tex thesis.bib
		pdflatex thesis7
		bibtex thesis7
		pdflatex thesis7
		pdflatex thesis7

thesis8.ps	: thesis8.dvi
		dvips -o thesis8.ps thesis8

thesis8.dvi	: thesis8.tex
		latex thesis8
		latex thesis8

thesis8.pdf	: thesis8.tex
		pdflatex thesis8
		pdflatex thesis8

thesis9.pdf	: thesis9.tex thesisglo.ist
		pdflatex thesis9
		makeindex -t thesis9.glg -o thesis9.gls -s thesisglo.ist thesis9.glo
		pdflatex thesis9

thesis9.dvi	: thesis9.tex thesisglo.ist
		latex thesis9
		makeindex -t thesis9.glg -o thesis9.gls -s thesisglo.ist thesis9.glo
		latex thesis9

thesis9.ps	: thesis9.dvi
		dvips -o thesis9.ps thesis9

thesis10.pdf	: thesis10.tex 
		pdflatex thesis10
		makeindex -t thesis10.glg -o thesis10.gls -s thesis10.ist thesis10.glo
		pdflatex thesis10
		pdflatex thesis10

thesis10.dvi	: thesis10.tex
		latex thesis10
		makeindex -t thesis10.glg -o thesis10.gls -s thesis10.ist thesis10.glo
		latex thesis10
		latex thesis10

thesis10.ps	: thesis10.dvi
		dvips -o thesis10.ps thesis10

clean	:
	\rm -f *.{lof,lot,loa,toc,aux,log,dvi,bbl,blg,ps,pdf,glg,gly,glo}
	\rm -f thesis10.ist
