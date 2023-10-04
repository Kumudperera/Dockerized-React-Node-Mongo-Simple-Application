FROM node:14

WORKDIR /app

COPY package.json .

RUN npm install

COPY . .

ENV LOCAL_DOMAIN=0.0.0.0:81

EXPOSE 3000

CMD ["npm", "start"]


