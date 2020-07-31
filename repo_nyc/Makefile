PROJ=taxi_schematic

${PROJ}.svg: crop.pdf
	pdf2svg crop.pdf ${PROJ}.svg

crop.pdf: ${PROJ}-rotated90.pdf
	pdfcrop --margins '0 0 0 0' --clip ${PROJ}-rotated90.pdf crop.pdf

${PROJ}-rotated90.pdf: ${PROJ}.pdf
	pdf90 ${PROJ}.pdf

${PROJ}.pdf: ${PROJ}.obj
	tgif -print -pdf -color ${PROJ}.obj
