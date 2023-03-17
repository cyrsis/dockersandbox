FROM node:latest@sha256:2405a991a6d9f6ac1d991feefc0a4539d5187abd2ca532fd18f7185c98b32a45
WORKDIR app
RUN npm install -g nodemon
COPY package.json .
RUN npm install
RUN mv /app/node_modules /node_modules
COPY . .
EXPOSE 80
CMD ["nodemon", "server.js"]
