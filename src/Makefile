###
### Makefile for building and pushing site
###

GITHUB_PAGES_BRANCH=gh-pages
THEME = biocs
THEMES22 = biocs-s22

MARKDOWN = python3 -m markdown
BASEDIR = .
LATEXDIR = $(BASEDIR)/latex
DOCSDIR = $(BASEDIR)/docs
PAGEDIR = $(BASEDIR)/content/
LATEXIFY = python3 $(LATEXDIR)/utils/latexify.py

html:
	hugo --theme=$(THEME)

s22:
	hugo --config config-s22.toml --theme=$(THEMES22) --contentDir content-s22 --layoutDir layouts-s22 --destination public-s22
	mv public-s22 ../s22


develop:
	sleep 1 && echo "Opening local browser..." &&  open http://localhost:1313 &
	hugo server --theme=$(THEME) --buildDrafts --watch

github: html
	cp -r ./docs ./public/
	cp -r ./public/* ../
	git add -A :/; git commit -m "Rebuilt site" ; git push

.PHONY: html clean develop
