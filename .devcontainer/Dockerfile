#FROM pytorch/pytorch
#FROM pytorch/pytorch:1.13.1-cuda11.6-cudnn8-devel
#FROM pytorch/pytorch:2.0.0-cuda11.7-cudnn8-devel
FROM pytorch/pytorch

RUN apt-get update && apt-get install -y xz-utils vim tcpdump git make

WORKDIR /
COPY requirements.txt requirements.txt  


RUN conda install -y pip
RUN pip install  -r requirements.txt
EXPOSE 80

RUN echo "set -o vi" >> /root/.bashr