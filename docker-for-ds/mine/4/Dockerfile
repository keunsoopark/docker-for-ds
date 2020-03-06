FROM continuumio/miniconda3

LABEL maintainer="Keunsoo Park <keunsoop.work@gmail.com>"
LABEL description="Dev environement for ML and DS team \
                   with access to shared data in network drive."

WORKDIR /data

RUN conda install jupyter -y && \
    conda install python==3.7.3 -y && \
    conda install pandas==0.24.2 -y && \
    conda install seaborn==0.9.0 -y && \
    conda clean -y --all

EXPOSE 8888

VOLUME /data

CMD ["jupyter", "notebook", "--ip=0.0.0.0", "--port=8888", "--no-browser", "--allow-root"]

# To run any files in WORKDIR > docker container run -it -v $(pwd):/data c7b7968ae3e6 bash
# To use notebook > docker container run -it -v $(pwd):/data -p 8888:8888 dev-env
