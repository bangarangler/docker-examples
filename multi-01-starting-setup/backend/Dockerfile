FROM node

WORKDIR /app

COPY package.json .

RUN npm install

COPY . .

EXPOSE 80

ENV MONGODB_USERNAME=root
ENV MONGODB_PASSWORD=secret

CMD [ "npm", "start" ]

# Run Mongo with data persist logs and on a network. env vars,
# docker run --name mongodb -v goals-data:/data/db --rm -d --network goals-net -e MONGO_INITDB_ROOT_USERNAME=jon -e MONGO_INITDB_ROOT_PASSWORD=secret mongo

# Run Node backend name goals-backend bind mount (move backend into container at
# /app) persist logs from logs folder and inside container at /app/logs. using
# env var. rm on container shutdown connected on goals-net publishing port 80
# from goals node image
#docker run --name goals-backend -v /Users/jonathanpalacio/Desktop/side-projects/acadeDocker/multi-01-starting-setup/backend:/app -v logs:/app/logs -v /app/node_modules -e MONGODB_USERNAME=jon -d --rm --network goals-net -p 80:80 goals-node
