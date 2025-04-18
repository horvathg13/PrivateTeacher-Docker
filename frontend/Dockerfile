FROM node:18-alpine

WORKDIR /app

RUN apk upgrade &&\
    apk add git

COPY ./package.json .
RUN git clone https://github.com/horvathg13/PrivateTeacher_Frontend.git
RUN cd PrivateTeacher_Frontend

WORKDIR /app/PrivateTeacher_Frontend
RUN npm install
RUN npm install -g serve

EXPOSE 3000

CMD ["serve","-s","build"]
