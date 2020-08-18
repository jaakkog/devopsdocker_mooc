FROM ubuntu:16.04

RUN apt-get update && apt-get install -y curl git

RUN git clone https://github.com/docker-hy/frontend-example-docker.git /dist

WORKDIR /dist

RUN curl -sL https://deb.nodesource.com/setup_10.x | bash && apt install -y nodejs

RUN npm -v && node -v && npm install 

ENV API_URL=http://localhost:8000

CMD ["npm", "start"]
