FROM node:12.18

WORKDIR /app

RUN npm init -y 

RUN apt-get update && \
    npm install 

RUN npm install puppeteer

RUN apt-get update && apt-get install -y libgtk-3.0 && \
    apt-get install -y libgbm-dev && \ 
    apt-get install -y libnss3 && \
    apt-get install -y libatk-bridge2.0-0 && \
    apt-get install -y libasound2

ENV LANG ja_JP.UTF-8

RUN apt-get update && \
    apt-get -y install locales fonts-ipafont fonts-ipaexfont && \
    echo "ja_JP UTF-8" > /etc/locale.gen && locale-gen