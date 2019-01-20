THISDIR := otherbook
THISBOOK := $(THISDIR)

export BOOKSUBVER := 1
export BOOKMAJVER := 0
export REVISIONNUMBER := 9

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

include ../latex/make.rules

figures/%.png: %.png
	cp $< $@

vpath %.png $(ORIG_FIGURE_DIRS)
