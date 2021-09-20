FROM ubuntu:18.04

RUN apt update && apt install -y curl
RUN curl -sL https://deb.nodesource.com/setup_14.x | bash
RUN apt install -y nodejs

EXPOSE 3000

WORKDIR /usr/src/app
COPY ./react-carousel-demo ./

RUN npm install
RUN npm audit fix

CMD ["npm", "start"]
