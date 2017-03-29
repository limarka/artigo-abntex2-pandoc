require 'rake/clean'
 
ARTIGO_LATEX = "xxx-artigo.tex"


desc "Gera e executa compilacao do artigo"
task :compilacao do
  system "pandoc -f markdown+raw_tex artigo.md --data-dir=. --template=artigo-abntex2 -o #{ARTIGO_LATEX}"
  system "latexmk -f -silent -pdf #{ARTIGO_LATEX}"
end

task :default => [:compilacao]

CLEAN.include(FileList["xxx*"])
