FROM ubuntu:latest

MAINTAINER oscar

RUN apt-get update && apt-get --no-install-recommends install -y \
                ca-certificates \
		biber \
		latexmk \
		make \
                emacs \
                texlive-bibtex-extra \
                texlive-fonts-recommended \
                texlive-generic-recommended \
                texlive-latex-base \
                texlive-latex-extra \
                texlive-latex-recommended \
                texlive-publishers \
                texlive-science \
                cm-super \
    && apt-get clean \
    && apt-get autoremove \
    && rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*

WORKDIR /data
VOLUME ["data"]