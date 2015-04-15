task :default => [:make, :clean]

task :make do
  `pdflatex main`
  `biber main`
  `pdflatex main`
  `open main.pdf`
end

task :clean do
  `latexmk -c main.tex`
  `rm  main.bbl main.run.xml`
  biber_cache = `biber --cache`
  `rm -rf #{biber_cache}`
end
