FROM node

WORKDIR /app
COPY . /app

RUN curl -sL https://deb.nodesource.com/setup_10.x | bash
RUN apt install -y nodejs
RUN npm install

ENV FRONT_URL=http://localhost:5000
EXPOSE 8000
ENTRYPOINT npm start

