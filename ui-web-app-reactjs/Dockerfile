FROM node:8
MAINTAINER sandeepdas8080@gmail.com Sandeep Das


WORKDIR /app

#copy local to docker
COPY . .

RUN npm install express
RUN npm install

EXPOSE 8080

#Runs in development Mode
CMD ["npm", "start"]