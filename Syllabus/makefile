PDFS := $(patsubst %.md,%.md.pdf,$(wildcard *.md))

PREFIX = /Users/lmp/Dropbox/AcademicWork/Pandoc_Templates
# /Users/lmp/ if using Macbook Pro

CSL = chicago-fullnote-bibliography

## Bibliography

BIB = /Users/lmp/Dropbox/AcademicWork/Bibs/refs.bib

all : $(PDFS)

%.md.pdf : %.md
	pandoc --pdf-engine=xelatex $< \
	--template=$(PREFIX)/Misc/syllabus.latex \
	-o $@ && open $@

clean:
	rm -rf *.pdf *.html *.log *.aux auto/
rebuild:
	make clean && make
