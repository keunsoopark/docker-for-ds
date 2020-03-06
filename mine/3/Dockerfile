FROM python:3.7.3-slim
LABEL maintainer="Keunsoo Park <keunsoop.work@gmail.com>"
LABEL version="0.1"
LABEL description: "Notebook and data (.csv file) to provide a summary \
                    of the total medals won by participating countries \
                    in the 2008 Summer Olympics."

# WORKDIR: working directory for any run, command, entry point, copy and add instructions that falls into the Dockerfile.
# cf) Always use the absolute path for WORKDIR
WORKDIR /data

# COPY: copy new files from source and add them to the file system of the container at the path destination.
COPY . /data

# RUN: execute any commands in a new layer on the top of current image and commits the results.
RUN pip install numpy pandas seaborn jupyter

# EXPOSE: indicates the ports in which a container listens for connection.
EXPOSE 8888

# There can be only one CMD instruction in a Dockerfile.
# To tell the container what to do after launching.
CMD ["jupyter", "notebook", "--ip=0.0.0.0", "--port=8888", "--no-browser", "--allow-root"]
