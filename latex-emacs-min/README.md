# Minimal latex + Emacs + orgmode image

Where minimal is to my requirements and not based on getting the smallest
image.


## Just latex

### Use for gitlab

Include this job in `.gitlab.yml`
```yaml
compile_pdf:
  image: najeraoscar/latex-emacs-min
  script:
    - latexmk -pdf file.tex
  artifacts:
    paths:
      - file.pdf
```
### Use locally

```bash
docker run -v $PWD:/data najeraoscar/latex-emacs-min latexmk -pdf file.tex
```

### Using org-mode

```yaml
image: najeraoscar/latex-emacs-min
compile_pdf:
  script:
    - emacs --batch -Q --script mycustomexport.el
  artifacts:
    paths:
      - file.pdf
```

In this case you are responsible of implementing `mycustomexport.el` to do
whatever needed for the export.
