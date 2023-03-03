FROM mcr.microsoft.com/devcontainers/ubuntu

RUN apt-get update && apt-get install -y \
    php5-mcrypt \
    python-pip

RUN pip install -r requirements.txt

RUN sudo wget -P /etc/apt/trusted.gpg.d https://cli-dist.keboola.com/deb/keboola.gpg
RUN echo "deb https://cli-dist.keboola.com/deb /" | sudo tee /etc/apt/sources.list.d/keboola.list
RUN sudo apt-get update
RUN sudo apt-get install keboola-cli
