FROM node

WORKDIR /app

COPY package.json .

RUN npm install

COPY . .

EXPOSE 3000

CMD [ "npm", "start" ]

# name goals-frontend bind mount for local dev moving frontend folder into
# container at /app/src rm if container stops publishing port 3000. using -it
# for interactive tty from goals-react image
# docker run --name goals-frontend -v /Users/jonathanpalacio/Desktop/side-projects/acadeDocker/multi-01-starting-setup/frontend/src:/app/src --rm -p 3000:3000 -it goals-react
