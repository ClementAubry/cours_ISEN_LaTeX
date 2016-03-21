# * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * *
#
# Make file simple pour LaTeX
#
# 	Compilation complete du document
#
# * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * *

# fichier principal
OUTDIR=Build
# compilateur latex
CC=pdflatex

# defaut = aide :
help:
	@echo
	@echo " Compilation du rapport, regles :"
	@echo
	@echo " all        : compile et met la biblio et les references a jour (long)"
	@echo " purge      : effacement des fichiers autres que .tex et .pdf (.aux .log .out .toc ..."
	@echo " compress   : compression par ghost script avec le parametrage qui va bien ..."
	@echo
	@echo

# compilation complete, on passe plusieurs fois pour les references croisee plus bibtex pour la
# biblio
all: $(TEX).tex
	@mkdir -p $(OUTDIR)
	$(CC) -output-directory=$(OUTDIR) $(TEX)
	@-if grep "\\citation" ./Build/$(TEX).aux > /dev/null; then \
		if bibtex -terse ./Build/$(TEX).aux; then \
			echo "bibtex: citation(s) founded"; \
			bibtex $(OUTDIR)/$(TEX) \
		else \
			echo "bibtex: NO citation founded"; \
		fi; \
	fi
	$(CC) -output-directory=$(OUTDIR) -synctex=1 --shell-escape $(TEX)
	@cp $(OUTDIR)/$(TEX).pdf $(TEX).pdf
	@cp $(OUTDIR)/$(TEX).synctex.gz $(TEX).synctex.gz
	@echo
	@echo
	@echo "fin ;)"
	@echo

compress: $(TEX).tex
	@gs -q -dSAFER -dNOPAUSE -dBATCH -sDEVICE=pdfwrite -dColorConversionStrategy=/LeaveColorUnchanged -dPDFSETTINGS=/default -sOUTPUTFILE=$(TEX)_compress.pdf -f $(TEX).pdf

# efface les fichiers .log .aux .toc .bbl .blg
.PHONY: purge
purge:
	@rm -vf Build/*
	@echo "clear"

