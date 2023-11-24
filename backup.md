

pandoc --standalone \
        --from markdown --to context \
        --variable papersize=letter \



pandoc -s \
        --from=markdown \
         -V geometry:margin=2.5cm \
        markdown/resume.md \         
        -o output/resume.pdf



-V colorlinks=true \
-V linkcolor=blue

<!-- CV  -->
pandoc -s -V geometry:margin=2.5cm -V colorlinks=true -V linkcolor=blue --variable papersize=letter markdown/resume.md -o output/resume.pdf

<!-- Cover letter -->
pandoc -s -V geometry:margin=2.5cm -V colorlinks=true -V linkcolor=blue --variable papersize=letter markdown/coverletter.md -o output/coverletter.pdf


pdflatex -s output/resume.tex -o output/resume.pdf