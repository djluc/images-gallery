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

## am adaugat urmatoarea linie pentru a rezolva eroarea (EACCES: permission denied, mkdir '/app/node_modules/.cache') din browser aparuta dupa folosirea Volumes

RUN mkdir /app/node_modules/.cache && chmod -R 777 /app/node_modules/.cache

COPY . ./

CMD ["npm", "start"]
