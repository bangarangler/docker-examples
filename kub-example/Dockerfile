FROM node:14

WORKDIR /app

COPY package.json .

RUN npm install

COPY . .

ENV PORT 80

EXPOSE $PORT

# VOLUME [ "/app/node_modules" ]
# VOLUME [ "/app/temp" ]

CMD ["npm", "start"]

# docker run -d -p 3000:80 --rm --name feedback-app -v feedback:/app/feedback -v "/Users/jonathanpalacio/Desktop/side-projects/acadeDocker/data-volumes-o1-starting-setup:/app:ro" -v /app/node_modules feedback-node:volumes