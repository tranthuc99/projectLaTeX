REMOVE=\rm -f
COPY=\cp

doc	: thesis_a4.pdf thesis_screen.pdf

html	: thesis.ps thesis/thesis.html

www	: thesis.ps thesis_a4.pdf thesis_screen.pdf thesis/thesis.html source
	$(COPY) thesis/*.{html,png,css} $(HOME)/www/latex/thesis/
	$(COPY) examples/*.{tex,bib,cls,html,ist} $(HOME)/www/latex/thesis/examples/
	$(COPY) examples/Makefile $(HOME)/www/latex/thesis/examples/
	$(COPY) examples/examples.tar.gz $(HOME)/www/latex/thesis/examples/
	$(COPY) pictures/*.png $(HOME)/www/latex/thesis/pictures/
	$(COPY) thesis_*.pdf $(HOME)/www/latex/thesis/
	$(COPY) thesis.tar.gz $(HOME)/www/latex/thesis/

source	: examples/examples.tar.gz thesis.tar.gz

examples/examples.tar.gz	:
				tar cvf examples/examples.tar examples/*.{tex,ist,bib,sty,html} examples/Makefile
				gzip examples/examples.tar

thesis.tar.gz	:
		tar cvf thesis.tar thesis.{tex,ist} preamble.tex pdfstuff.sty imgsource Makefile examples ueacrest.pdf
		gzip thesis.tar

thesis.ps	: thesis.dvi
		dvips -o thesis.ps thesis

thesis.dvi	: thesis.tex thesis.ist pdfstuff.sty preamble.tex \
		  examples/thesis1.tex \
		  examples/thesis.bib
		$(REMOVE) thesis.{toc,aux,lof,lot,ind}
		latex thesis
		makeindex -s thesis.ist thesis.idx
		latex thesis
		latex thesis

thesis_a4.pdf	: thesis.tex thesis.ist pdfstuff.sty preamble.tex \
		  examples/thesis1.tex \
		  examples/thesis.bib
		$(REMOVE) thesis.{aux,lot,lof,toc,ind}
		echo "\screenfalse" > switch.tex
		pdflatex thesis
		makeindex -s thesis.ist thesis.idx
		pdflatex thesis
		pdflatex thesis
		$(COPY) thesis.pdf thesis_a4.pdf

thesis_screen.pdf	: thesis.tex thesis.ist pdfstuff.sty preamble.tex \
			  examples/thesis1.tex \
			  examples/thesis.bib
			$(REMOVE) thesis.{aux,lot,lof,toc,ind}
			echo "\screentrue" > switch.tex
			pdflatex thesis
			makeindex -s thesis.ist thesis.idx
			pdflatex thesis
			pdflatex thesis
			$(COPY) thesis.pdf thesis_screen.pdf

thesis/thesis.html	: thesis.tex
			latex2html -link 3 -split 6 \
			-local_icons \
			-nofootnode \
                        -transparent -white \
			-address "N.L.C. Talbot. School of Computing Sciences. University of East Anglia." \
			-up_url "../index.html" \
			-up_title "LaTeX Related Information" \
			-top_navigation -bottom_navigation \
			-info "This document was generated using the <a href=http://www.latex2html.org>LaTeX2HTML</a> translator." \
			thesis 

squeaky :
	$(REMOVE) thesis/thesis.{css,html}
	$(REMOVE) thesis/images.{tex,aux,log,idx}
	$(REMOVE) thesis/index.html
	$(REMOVE) thesis/img*.png
	$(REMOVE) thesis/*.pl
	$(REMOVE) thesis/node*.html
	$(REMOVE) thesis_a4.pdf thesis_screen.pdf

clean	:
	$(REMOVE) thesis.{ps,pdf,dvi,aux,log,ind,ilg,idx,toc,lof,lot,loe,out}
