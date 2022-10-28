# Uma possível solução para o segundo desafio

FROM ubuntu:20.04

RUN apt-get update -y

RUN apt-get install -y git python3 python3-pip

RUN git clone \
https://github.com/Malware-Hunter/sbseg22-feature-selection.git

WORKDIR /sbseg22-feature-selection

RUN pip install --user pandas numpy scikit-learn

