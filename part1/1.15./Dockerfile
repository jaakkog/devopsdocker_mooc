FROM ubuntu:16.04

RUN apt-get update && apt-get install -y curl git

RUN git clone https://github.com/jaakkog/wine-app.git /mydir

WORKDIR /mydir

RUN curl -sL https://deb.nodesource.com/setup_10.x | bash && apt install -y nodejs

RUN npm -v && node -v && npm install 

EXPOSE 3000

CMD ["npm", "start"]