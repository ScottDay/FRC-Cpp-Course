# Latex Makefile for Linux and Windows
# http://stackoverflow.com/questions/4058840/makefile-that-distincts-between-windows-and-unix-like-systems

FILENAME = lecture4-functions.tex
OS := $(shell uname)

ifeq ($(OS), Linux)
	COMPILER = xelatex
	RM = rm -f
	FixPath = $1
else
	ifeq ($(OS), Windows)
		COMPILER = xelatex.exe
		RM = del /Q
		FixPath = $(subst /,\,$1)
	endif
endif

compileropts = -synctex=1 -interaction=nonstopmode -shell-escape

# ----------

all: compile clean

compile: ${compiler} ${compileropts} ${FILENAME}

clean: RM ${FILENAME}.{ps,log,aux,out,dvi,bbl,blg,synctex.gz,listing,nav,snm,toc,vrb}
	RM _minted-lecture1-introduction

clean-all: clean
	RM ${FILENAME}.pdf
