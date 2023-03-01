FROM node:latest@sha256:83841d113e09345a28b146e431f15b062341c5449218e501ba45ef8f9cff6049
WORKDIR app
RUN npm install -g nodemon
COPY package.json .
RUN npm install
RUN mv /app/node_modules /node_modules
COPY . .
EXPOSE 80
CMD ["nodemon", "server.js"]
