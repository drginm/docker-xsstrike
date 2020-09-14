FROM continuumio/anaconda3

WORKDIR /workdir

RUN apt-get install -y unzip

ADD https://github.com/s0md3v/XSStrike/archive/master.zip ./

RUN unzip master.zip && \
    rm master.zip

RUN conda config --append channels conda-forge && \
    conda install fuzzywuzzy requests

ENTRYPOINT ["python", "./XSStrike-master/xsstrike.py"]
