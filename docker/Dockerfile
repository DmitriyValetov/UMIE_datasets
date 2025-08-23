FROM python:3.11.13

ENV DEBIAN_FRONTEND=noninteractive

RUN apt-get update
RUN apt-get upgrade -y
RUN apt-get install git ffmpeg libsm6 libxext6
RUN pip3 install datasets poetry scikit-learn jsonlines opencv-python pillow pydicom nibabel bs4

WORKDIR /
RUN git clone https://github.com/TheLion-ai/UMIE_datasets.git
WORKDIR /UMIE_datasets
RUN poetry install

WORKDIR /develop