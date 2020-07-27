pictures.svg: crop.pdf
	pdf2svg crop.pdf pictures.svg

crop.pdf: pictures-rotated90.pdf
	pdfcrop --margins '0 0 0 0' --clip pictures-rotated90.pdf crop.pdf

pictures-rotated90.pdf: pictures.pdf
	pdf90 pictures.pdf 

pictures.pdf: pictures.obj
	tgif -print -pdf pictures.obj
