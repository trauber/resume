all:
	echo "Targets are: cli, gui"
cli:
	./y2j-python.sh resume-cli.yaml > resume.json
	#./y2j-ruby.sh resume-cli.yaml > resume.json
	sed -i -e '/thirty/ r dynsum.json' resume.json
	## cat resume-latex.hbs | handlebars resume.json > tmp.tex
	## cat resume-txt.hbs | handlebars resume.json | fmt - > tmp.txt
	handlebars resume.json < resume-latex.hbs > tmp.tex
	handlebars resume.json < resume-txt.hbs | fmt - > tmp.txt

	sed -f preproc.sed tmp.tex > resume-rich-traube.tex
	#sed -f cli.sed tmp.tex > resume-rich-traube.tex
	sed -f preproc-text.sed tmp.txt > resume-rich-traube.txt
	## cat resume-md.hbs | handlebars resume.json > tmp.md
	handlebars resume.json < resume-md.hbs > tmp.md
	sed -f preproc-text.sed  tmp.md > resume-rich-traube.md
	pandoc --reference-docx=reference.docx -S -o ../output/cli/resume-rich-traube.docx resume-rich-traube.md
	pandoc -S -o ../output/cli/resume-rich-traube.odt resume-rich-traube.md
	pandoc -S --template=template.rtf -s -o tmp.rtf resume-rich-traube.md
	cat tmp.rtf | awk -f rtf.awk > ../output/cli/resume-rich-traube.rtf
	## cat resume-txt.hbs | handlebars resume.json | fmt - | awk -f text-postproc.awk > tmp.txt
	handlebars resume.json < resume-txt.hbs | fmt - | awk -f text-postproc.awk > tmp.txt
	cat -s tmp.txt > ../output/cli/resume-rich-traube.txt
	pdflatex resume-rich-traube
	mv resume-rich-traube.pdf ../output/cli/

emsl:
	./y2j-ruby.sh resume-cli.yaml > resume.json
	sed -i -e '/extensive/ r dynsum-emsl-2016-09-12.json' resume.json
	cat resume-latex.hbs | handlebars resume.json > tmp.tex
	cat resume-txt.hbs | handlebars resume.json | fmt - > tmp.txt
	sed -f preproc.sed tmp.tex > resume-rich-traube.tex
	#sed -f cli.sed tmp.tex > resume-rich-traube.tex
	sed -f preproc-text.sed tmp.txt > resume-rich-traube.txt
	cat resume-md.hbs | handlebars resume.json > tmp.md
	sed -f preproc-text.sed  tmp.md > resume-rich-traube.md
	pandoc --reference-docx=reference.docx -S -o ../output/cli/resume-rich-traube.docx resume-rich-traube.md
	pandoc -S -o ../output/cli/resume-rich-traube.odt resume-rich-traube.md
	pandoc -S --template=template.rtf -s -o tmp.rtf resume-rich-traube.md
	cat tmp.rtf | awk -f rtf.awk > ../output/cli/resume-rich-traube.rtf
	cat resume-txt.hbs | handlebars resume.json | fmt - | awk -f text-postproc.awk > tmp.txt
	cat -s tmp.txt > ../output/cli/resume-rich-traube.txt
	pdflatex resume-rich-traube
	mv resume-rich-traube.pdf ../output/cli/

upenn:
	./y2j-ruby.sh resume-cli.yaml > resume.json
	sed -i -e '/thirty/ r dynsum-upenn-2016-07-11.json' resume.json
	cat resume-latex.hbs | handlebars resume.json > tmp.tex
	cat resume-txt.hbs | handlebars resume.json | fmt - > tmp.txt
	sed -f preproc.sed tmp.tex > resume-rich-traube.tex
	#sed -f cli.sed tmp.tex > resume-rich-traube.tex
	sed -f preproc-text.sed tmp.txt > resume-rich-traube.txt
	cat resume-md.hbs | handlebars resume.json > tmp.md
	sed -f preproc-text.sed  tmp.md > resume-rich-traube.md
	pandoc --reference-docx=reference.docx -S -o ../output/cli/resume-rich-traube.docx resume-rich-traube.md
	pandoc -S -o ../output/cli/resume-rich-traube.odt resume-rich-traube.md
	pandoc -S --template=template.rtf -s -o tmp.rtf resume-rich-traube.md
	cat tmp.rtf | awk -f rtf.awk > ../output/cli/resume-rich-traube.rtf
	cat resume-txt.hbs | handlebars resume.json | fmt - | awk -f text-postproc.awk > tmp.txt
	cat -s tmp.txt > ../output/cli/resume-rich-traube.txt
	pdflatex resume-rich-traube
	mv resume-rich-traube.pdf ../output/cli/

northwood:
	./y2j-ruby.sh resume-cli.yaml > resume.json
	sed -i -e '/thirty/ r northwood-sum.json' resume.json
	cat resume-latex.hbs | handlebars resume.json > tmp.tex
	cat resume-txt.hbs | handlebars resume.json | fmt - > tmp.txt
	sed -f preproc.sed tmp.tex > resume-rich-traube.tex
	#sed -f cli.sed tmp.tex > resume-rich-traube.tex
	sed -f preproc-text.sed tmp.txt > resume-rich-traube.txt
	cat resume-md.hbs | handlebars resume.json > tmp.md
	sed -f preproc-text.sed  tmp.md > resume-rich-traube.md
	pandoc --reference-docx=reference.docx -S -o ../output/northwood/resume-rich-traube.docx resume-rich-traube.md
	pandoc -S -o ../output/northwood/resume-rich-traube.odt resume-rich-traube.md
	pandoc -S --template=template.rtf -s -o tmp.rtf resume-rich-traube.md
	cat tmp.rtf | awk -f rtf.awk > ../output/northwood/resume-rich-traube.rtf
	cat resume-txt.hbs | handlebars resume.json | fmt - | awk -f text-postproc.awk > tmp.txt
	cat -s tmp.txt > ../output/northwood/resume-rich-traube.txt
	pdflatex resume-rich-traube
	mv resume-rich-traube.pdf ../output/northwood/



gui:
	./y2j-ruby.sh resume-gui.yaml > resume.json
	sed -i -e '/thirty/ r dynsum.json' resume.json
	cat resume-latex.hbs | handlebars resume.json > tmp.tex
	cat resume-txt.hbs | handlebars resume.json | fmt - > tmp.txt
	sed -f preproc.sed tmp.tex > resume-rich-traube.tex
	sed -f preproc-text.sed tmp.txt > resume-rich-traube.txt
	cat resume-md.hbs | handlebars resume.json > tmp.md
	sed -f preproc-text.sed  tmp.md > resume-rich-traube.md
	pandoc --reference-docx=reference.docx -S -o ../output/gui/resume-rich-traube.docx resume-rich-traube.md
	pandoc -S -o ../output/gui/resume-rich-traube.odt resume-rich-traube.md
	pandoc -S --template=template.rtf -s -o tmp.rtf resume-rich-traube.md
	cat tmp.rtf | awk -f rtf.awk > ../output/gui/resume-rich-traube.rtf
	cat resume-txt.hbs | handlebars resume.json | fmt - | awk -f text-postproc.awk > tmp.txt
	cat -s tmp.txt > ../output/gui/resume-rich-traube.txt
	pdflatex resume-rich-traube
	mv resume-rich-traube.pdf ../output/gui/
