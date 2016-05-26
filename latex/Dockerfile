FROM ubuntu:14.04
MAINTAINER I Putu Pradnyana <saintrx@gmail.com>
RUN echo ttf-mscorefonts-installer msttcorefonts/accepted-mscorefonts-eula select true | debconf-set-selections
RUN apt-get update && apt-get install -y texlive \
		texlive-xetex \
		texlive-lang-other \
		python \
		python-pip \
		xzdec \
		&& apt-get --reinstall install ttf-mscorefonts-installer
RUN pip install pygments
RUN tlmgr init-usertree && tlmgr install minted \
		lineno \
		xcolor \
		tocbibind
