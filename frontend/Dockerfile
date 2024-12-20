## din ce imagine creem imaginea noastra
FROM node:15.14-alpine
## folderul in care se salveaza fisierele de aplicatie
WORKDIR /app
## portul pe care-l exportam
EXPOSE 3000
## se intaleaza toate dependintele

COPY package.json ./
COPY package-lock.json ./

RUN npm install --silent

COPY . ./

CMD ["npm", "start"]
