REMOVE=\rm -f
COPY=\cp
MOVE=\mv

pictures	: eps png pdf

png		: ../pictures/bibabbrv.png \
		  ../pictures/bibalpha.png \
		  ../pictures/bibapalike.png \
		  ../pictures/bibplain.png \
		  ../pictures/bibacm.png \
		  ../pictures/bibieeetr.png \
		  ../pictures/bibunsrt.png \
		  ../pictures/titlepage.png \
		  ../pictures/algorithm.png 

eps		: ../pictures/bibabbrv.eps \
		  ../pictures/bibalpha.eps \
		  ../pictures/bibplain.eps \
		  ../pictures/bibacm.eps \
		  ../pictures/bibieeetr.eps \
		  ../pictures/bibunsrt.eps \
		  ../pictures/titlepage.ps \
		  ../pictures/algorithm.eps \
		  ../pictures/titlepage.ps

pdf		: ../pictures/bibabbrv.pdf \
		  ../pictures/bibalpha.pdf \
		  ../pictures/bibplain.pdf \
		  ../pictures/bibacm.pdf \
		  ../pictures/bibieeetr.pdf \
		  ../pictures/bibunsrt.pdf \
		  ../pictures/titlepage.ps \
		  ../pictures/algorithm.pdf \
		  ../pictures/titlepage.pdf

titlepage.dvi	: titlepage.tex
		latex titlepage

titlepage.ps	: titlepage.dvi
		dvips -l =1 -o titlepage.ps titlepage

titlepage.pdf	: titlepage.ps
		epstopdf titlepage.ps > titlepage.pdf

../pictures/titlepage.ps	: titlepage.ps
				$(COPY) titlepage.ps ../pictures
				
../pictures/titlepage.png	: titlepage.png
			$(COPY) titlepage.png ../pictures

../pictures/titlepage.pdf	: titlepage.pdf
			$(COPY) titlepage.pdf ../pictures

titlepage.png	: titlepage.ps
		pstopnm titlepage.ps
		pnmtopng titlepage001.ppm > titlepage.png
		$(REMOVE) titlepage001.ppm

../pictures/bibplain.eps	: bibplain.dvi
				dvips -E -o ../pictures/bibplain.eps bibplain

../pictures/bibplain.pdf	: ../pictures/bibplain.eps
				epstopdf ../pictures/bibplain.eps > ../pictures/bibplain.pdf

bibplain.ps	: bibplain.dvi
		dvips -o bibplain.ps bibplain

bibplain.dvi	: bibplain.tex thesis.bib
		latex bibplain
		bibtex bibplain
		latex bibplain

../pictures/bibplain.png	: bibplain.png
			$(MOVE) bibplain.png ../pictures

bibplain.png	: bibplain.ps
		pstopnm bibplain.ps
		pnmcrop bibplain001.ppm > bibplain.crop.ppm
		pnmtopng bibplain.crop.ppm > bibplain.png
		$(REMOVE) bibplain001.ppm

../pictures/bibabbrv.eps	: bibabbrv.dvi
				dvips -E -o ../pictures/bibabbrv.eps bibabbrv

../pictures/bibabbrv.pdf	: ../pictures/bibabbrv.eps
				epstopdf ../pictures/bibabbrv.eps > ../pictures/bibabbrv.pdf

bibabbrv.ps	: bibabbrv.dvi
		dvips -o bibabbrv.ps bibabbrv

bibabbrv.dvi	: bibabbrv.tex thesis.bib
		latex bibabbrv
		bibtex bibabbrv
		latex bibabbrv

../pictures/bibabbrv.png	: bibabbrv.png
			$(MOVE) bibabbrv.png ../pictures

bibabbrv.png	: bibabbrv.ps
		pstopnm bibabbrv.ps
		pnmcrop bibabbrv001.ppm > bibabbrv.crop.ppm
		pnmtopng bibabbrv.crop.ppm > bibabbrv.png
		$(REMOVE) bibabbrv001.ppm

../pictures/bibalpha.eps	: bibalpha.dvi
				dvips -E -o ../pictures/bibalpha.eps bibalpha

../pictures/bibalpha.pdf	: ../pictures/bibalpha.eps
				epstopdf ../pictures/bibalpha.eps > ../pictures/bibalpha.pdf

bibalpha.ps	: bibalpha.dvi
		dvips -o bibalpha.ps bibalpha

bibalpha.dvi	: bibalpha.tex thesis.bib
		latex bibalpha
		bibtex bibalpha
		latex bibalpha

../pictures/bibalpha.png	: bibalpha.png
			$(MOVE) bibalpha.png ../pictures

bibalpha.png	: bibalpha.ps
		pstopnm bibalpha.ps
		pnmcrop bibalpha001.ppm > bibalpha.crop.ppm
		pnmtopng bibalpha.crop.ppm > bibalpha.png
		$(REMOVE) bibalpha001.ppm

../pictures/bibapalike.eps	: bibapalike.dvi
				dvips -E -o ../pictures/bibapalike.eps bibapalike

../pictures/bibapalike.pdf	: ../pictures/bibapalike.eps
				epstopdf ../pictures/bibapalike.eps > ../pictures/bibapalike.pdf

bibapalike.ps	: bibapalike.dvi
		dvips -o bibapalike.ps bibapalike

bibapalike.dvi	: bibapalike.tex thesis.bib
		latex bibapalike
		bibtex bibapalike
		latex bibapalike

../pictures/bibapalike.png	: bibapalike.png
			$(MOVE) bibapalike.png ../pictures

bibapalike.png	: bibapalike.ps
		pstopnm bibapalike.ps
		pnmcrop bibapalike001.ppm > bibapalike.crop.ppm
		pnmtopng bibapalike.crop.ppm > bibapalike.png
		$(REMOVE) bibapalike001.ppm

../pictures/bibacm.eps	: bibacm.dvi
			dvips -E -o ../pictures/bibacm.eps bibacm

../pictures/bibacm.pdf	: ../pictures/bibacm.eps
				epstopdf ../pictures/bibacm.eps > ../pictures/bibacm.pdf

bibacm.ps	: bibacm.dvi
		dvips -o bibacm.ps bibacm

bibacm.dvi	: bibacm.tex thesis.bib
		latex bibacm
		bibtex bibacm
		latex bibacm

../pictures/bibacm.png	: bibacm.png
			$(MOVE) bibacm.png ../pictures

bibacm.png	: bibacm.ps
		pstopnm bibacm.ps
		pnmcrop bibacm001.ppm > bibacm.crop.ppm
		pnmtopng bibacm.crop.ppm > bibacm.png
		$(REMOVE) bibacm001.ppm

../pictures/bibieeetr.eps	: bibieeetr.dvi
			dvips -E -o ../pictures/bibieeetr.eps bibieeetr

../pictures/bibieeetr.pdf	: ../pictures/bibieeetr.eps
				epstopdf ../pictures/bibieeetr.eps > ../pictures/bibieeetr.pdf

bibieeetr.ps	: bibieeetr.dvi
		dvips -o bibieeetr.ps bibieeetr

bibieeetr.dvi	: bibieeetr.tex thesis.bib
		latex bibieeetr
		bibtex bibieeetr
		latex bibieeetr

../pictures/bibieeetr.png	: bibieeetr.png
			$(MOVE) bibieeetr.png ../pictures

bibieeetr.png	: bibieeetr.ps
		pstopnm bibieeetr.ps
		pnmcrop bibieeetr001.ppm > bibieeetr.crop.ppm
		pnmtopng bibieeetr.crop.ppm > bibieeetr.png
		$(REMOVE) bibieeetr001.ppm

../pictures/bibunsrt.eps	: bibunsrt.dvi
			dvips -E -o ../pictures/bibunsrt.eps bibunsrt

../pictures/bibunsrt.pdf	: ../pictures/bibunsrt.eps
				epstopdf ../pictures/bibunsrt.eps > ../pictures/bibunsrt.pdf

bibunsrt.ps	: bibunsrt.dvi
		dvips -o bibunsrt.ps bibunsrt

bibunsrt.dvi	: bibunsrt.tex thesis.bib
		latex bibunsrt
		bibtex bibunsrt
		latex bibunsrt

../pictures/bibunsrt.png	: bibunsrt.png
			$(MOVE) bibunsrt.png ../pictures

bibunsrt.png	: bibunsrt.ps
		pstopnm bibunsrt.ps
		pnmcrop bibunsrt001.ppm > bibunsrt.crop.ppm
		pnmtopng bibunsrt.crop.ppm > bibunsrt.png
		$(REMOVE) bibunsrt001.ppm

../pictures/algorithm.png	: algorithm.png
				$(MOVE) algorithm.png ../pictures

algorithm.png	: algorithm.eps
		pstopnm -portrait algorithm.eps
		#pnmcrop algorithm.eps001.ppm > algorithm.crop.ppm
		#pnmtopng algorithm.crop.ppm > algorithm.png
		pnmtopng algorithm.eps001.ppm > algorithm.png
		$(REMOVE) algorithm001.ppm

../pictures/algorithm.eps	: algorithm.dvi
				dvips -E -o ../pictures/algorithm.eps algorithm

../pictures/algorithm.pdf	: algorithm.tex
				pdflatex algorithm
				$(COPY) algorithm.pdf ../pictures

algorithm.ps	: algorithm.dvi
		dvips -o algorithm.ps algorithm

algorithm.dvi	: algorithm.tex
		latex algorithm

clean	:
	$(REMOVE) *.{aux,log,dvi,bbl,blg,ps,png,ppm,pdf}
