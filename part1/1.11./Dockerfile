FROM ubuntu:16.04

RUN apt-get update && apt-get install -y curl git

RUN git clone https://github.com/docker-hy/backend-example-docker.git /mydir

WORKDIR /mydir

RUN curl -sL https://deb.nodesource.com/setup_10.x | bash && apt install -y nodejs

RUN npm -v && node -v && npm install 

ENV FRONT_URL=http://localhost:5000

CMD ["npm", "start"]