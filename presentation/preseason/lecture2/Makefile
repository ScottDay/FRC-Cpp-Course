# Latex Makefile for Windows

filename = lecture2-datatypesandvariables.tex

compiler     = xelatex.exe
compileropts = -synctex=1 -interaction=nonstopmode -shell-escape

pdfviewer = "C:\Program Files (x86)\Adobe\Acrobat DC\Acrobat\Acrobat.exe"



all: compile compile

compile: ${compiler} ${compileropts} ${filename}

read: ${pdfviewer} "${filename}"

clean: del ${filename}.{ps,pdf,log,aux,out,dvi,bbl,blg,synctex.gz,listing,nav,snm,toc,vrb}
	del _minted-lecture1-introduction
