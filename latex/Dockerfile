FROM ubuntu:latest

MAINTAINER oscar

RUN apt-get update && apt-get install -y \
		biber \
		latexmk \
		make \
		texlive-full \
    && apt-get clean \
    && apt-get autoremove \
    && rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
