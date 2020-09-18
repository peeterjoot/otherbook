THISDIR := otherbook
THISBOOK := $(THISDIR)

BIBLIOGRAPHY_PATH := classicthesis_mine
HAVE_OWN_CONTENTS := 1
#HAVE_OWN_TITLEPAGE := 1
MY_CLASSICTHESIS_FRONTBACK_FILES += ../latex/classicthesis_mine/FrontBackmatter/Index.tex
MY_CLASSICTHESIS_FRONTBACK_FILES += ../latex/classicthesis_mine/FrontBackmatter/ContentsAndFigures.tex
BOOKTEMPLATE := ../latex/classicthesis_mine/ClassicThesis2.tex

include make.revision
include ../latex/make.bookvars

FIGURES := ../figures/$(THISBOOK)

ORIG_FIGURE_DIRS += ../figures/classicalmechanics
ORIG_FIGURE_DIRS += ../figures/gabook

#LOCAL_FIGURE_FILES += hoopSpring.png
#LOCAL_FIGURE_FILES += parallelogramArea.png

SOURCE_DIRS += appendix
SOURCE_DIRS += $(FIGURES)
#SOURCE_DIRS += solutions

#GENERATED_SOURCES += mathematica.tex
GENERATED_SOURCES += backmatter.tex

include ../latex/make.rules

figures/%.png: %.png
	cp $< $@

vpath %.png $(ORIG_FIGURE_DIRS)

#backmatter.tex: ../latex/classicthesis_mine/backmatter_with_parts.tex
#	rm -f $@
#	ln -s ../latex/classicthesis_mine/backmatter_with_parts.tex backmatter.tex

backmatter.tex: ../latex/classicthesis_mine/backmatter2.tex
	rm -f $@
	ln -s ../latex/classicthesis_mine/backmatter2.tex backmatter.tex
