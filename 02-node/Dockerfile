# image locally or from dockerHub
# FROM name:tag
FROM node

WORKDIR /app

# host file system - image/container file system
# explciti
# COPY . /app

# if source code chaneges, not need run npm install
# because off it is a lawer layer
COPY package.json ./

# commands in image - in workdir
RUN npm install

# relative from workdir
COPY . ./

EXPOSE 80

# commands in container 
# executed not in the image but the container
# CMD is always the last instuction 
CMD ["node", "server.js"]