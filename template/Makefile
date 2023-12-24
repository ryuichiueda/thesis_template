main.pdf: main.dvi
	dvipdfmx main.dvi

main.dvi: *.tex
	sed -e 's/。/. /g' -e 's/、/, /g' -i *.tex
	cp main.tex tmp.tex
	platex tmp.tex
	pbibtex tmp.aux
	mendex tmp
	platex tmp.tex
	platex tmp.tex
	platex tmp.tex
	mv tmp.dvi main.dvi

clean:
	rm -f *.aux *.log *.dvi *.bbl *.blg *.ilg *.idx *.toc *.ind tmp.*
