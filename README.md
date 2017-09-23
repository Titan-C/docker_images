# Docker images

Docker images for testing software. This repo launches automatic builds on
docker hub.

## Scipy

Conda virtual envs with Python 2.7 & 3.6 with/out MKL

```bash
docker pull najeraoscar/scipy
```

## Latex

Texlive distribution

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
