# Docker images

Docker images for testing software. This repo launches automatic builds on
docker hub.

## Scipy

Conda virtual envs with Python 2.7 & 3.6 with/out MKL

```bash
docker pull najeraoscar/scipy
```
## latex-emacs-min

This is a lighter version of the Texlive distribution containing the
minimal for my usecase Texlive modules and Emacs. It uses about 1GB of disk
space. It can be used like the [Latex container](#latex)

```bash
docker pull najeraoscar/latex-emacs-min
```

## Latex

Texlive full distribution. This uses about 4GB of disk space

```bash
docker pull najeraoscar/latex
```

### Use for gitlab

Include this job in `.gitlab.yml`
```yaml
compile_pdf:
  image: najeraoscar/latex
  script:
    - latexmk -pdf file.tex
  artifacts:
    paths:
      - file.pdf
```

### Use locally

```bash
docker run -v $PWD:/data najeraoscar/latex latexmk -pdf file.tex
```
