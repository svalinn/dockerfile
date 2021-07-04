FROM ghcr.io/svalinn/pymoab-py2-18.04:latest

RUN apt-get -y --force-yes update \
    && apt-get install -y --fix-missing \
    wget \
    cpio \
    libpcre3-dev \
    libgl1-mesa-glx \
    libgl1-mesa-dev \
    libsm6 \
    libxt6 \
    libglu1-mesa \
    libharfbuzz-dev

RUN pip install xmldiff

RUN cd $HOME/opt \
    && wget https://github.com/visit-dav/visit/releases/download/v3.1.1/visit3_1_1.linux-x86_64-ubuntu18.tar.gz \
    && wget https://github.com/visit-dav/visit/releases/download/v3.1.1/visit-install3_1_1 \
    && echo 1 > input \
    && bash visit-install3_1_1 3.1.1 linux-x86_64-ubuntu18 /usr/local/visit < input \
    && rm -rf visit3_1_1.linux-x86_64-ubuntu18.tar.gz visit-install3_1_1

# set environment variables
ENV PATH /usr/local/visit/bin:$PATH
ENV LD_LIBRARY_PATH /usr/local/visit/3.1.1/linux-x86_64/lib/:$LD_LIBRARY_PATH
ENV PYTHONPATH /usr/local/visit/3.1.1/linux-x86_64/lib/site-packages:$PYTHONPATH
