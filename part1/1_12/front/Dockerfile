FROM node

WORKDIR /app
COPY . /app

RUN curl -sL https://deb.nodesource.com/setup_10.x | bash
RUN apt install -y nodejs
RUN npm install
ENV API_URL=http://localhost:8000
EXPOSE 5000
ENTRYPOINT npm start
