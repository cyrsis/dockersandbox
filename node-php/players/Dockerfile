FROM node:latest@sha256:83841d113e09345a28b146e431f15b062341c5449218e501ba45ef8f9cff6049
COPY package.json package.json
RUN npm install
COPY . .
EXPOSE 80
CMD ["node", "server.js"]
