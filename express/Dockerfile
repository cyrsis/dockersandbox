FROM node:latest@sha256:2405a991a6d9f6ac1d991feefc0a4539d5187abd2ca532fd18f7185c98b32a45
COPY package.json package.json
RUN npm install
COPY ./app ./app
CMD ["node", "app/server.js"]