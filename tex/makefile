DOC=vk9l-dx-scope

RESIDUE=$(wildcard *.acn *.acr *.alg *.aux *.bbl *.blg *.dvi *.glg *.glo *.gls *.idx *.ilg *.ind *.ist *.lof *.log *.lot *.out *.pdf *.bak *.toc *.pdf texput.log)

vk9l-dx-scope:
	xelatex $@
	xelatex $@
	makeindex $@
	bibtex vk9l-dx-scope
	makeglossaries $@
	xelatex $@
	xelatex $@

install:
	cp vk9l-dx-scope.pdf /var/www/w7brs/vk9l/scope.pdf
	cp vk9l-dx-scope.pdf /var/www/w7brs/vk9l/vk9l.pdf

clean:
	rm -f $(RESIDUE)
