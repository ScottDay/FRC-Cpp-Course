# Latex Makefile for Linux and Windows
# http://stackoverflow.com/questions/4058840/makefile-that-distincts-between-windows-and-unix-like-systems

FILE_NAME = lecture4-functions.tex
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

COMPILER_OPTS = -synctex=1 -interaction=nonstopmode -shell-escape

# ----------

all: compile clean

compile: ${compiler} ${COMPILER_OPTS} ${FILE_NAME}

clean: RM ${FILE_NAME}.{ps,log,aux,out,dvi,bbl,blg,synctex.gz,listing,nav,snm,toc,vrb}
	RM _minted-lecture1-introduction

clean-all: clean
	RM ${FILE_NAME}.pdf
