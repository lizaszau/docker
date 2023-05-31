FROM node:14

WORKDIR /app

COPY package.json .

RUN npm install

COPY . .

EXPOSE 80

# anonymus volume - deleted if container deleted
# but named container live over deleting container (run -v)
# equivalet with -v /app/feedback flag in run command
VOLUME ["/app/feedback"]
VOLUME ["/app/node_modules"]


CMD ["node", "server.js"]