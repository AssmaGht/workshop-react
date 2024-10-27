FROM node:21 
#directory mt3 el work fl container
WORKDIR /app

ENV DATABASE_URL=$DATABASE_URL

#first step
#c'est package contirnt des scripts ccontient les commandes nest cli
COPY ./package*.json ./
COPY ./tsconfig.json ./
#yemhi yanstali les commandes 
RUN npm install 
COPY ./ ./ 

RUN npm run build 

RUN npx prisma generate

CMD [ "npm", "run", "start:dev" ]