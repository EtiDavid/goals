FROM node

WORKDIR /app

COPY package.json .

RUN npm install


COPY . .

EXPOSE 80

#ENV MONGOURI=mongodb+srv://etidavid:Y9M8XfWNFGatLUGb@daviddb.jwihjz2.mongodb.net/goals?retryWrites=true&w=majority
ENV MONGOURI=mongodb+srv://etidavid:Y9M8XfWNFGatLUGb@daviddb.jwihjz2.mongodb.net/?appName=davidDB

#ENV MONGODB_PASSWORD=secret
#ENV MONGODB_URL=mongodb

CMD ["npm", "start"]