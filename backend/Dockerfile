FROM node

WORKDIR /app

COPY package.json .

RUN npm install


COPY . .

EXPOSE 80


#ENV MONGOURI=mongodb+srv://etidavid:Y9M8XfWNFGatLUGb@daviddb.jwihjz2.mongodb.net/?appName=davidDB



CMD ["npm", "start"]