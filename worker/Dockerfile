FROM node:alpine

WORKDIR "/app"

COPY ./package.json ./
RUN npm config set strict-ssl=false
RUN npm install

COPY . .

RUN chown -R node /app/node_modules

USER node

CMD [ "npm", "run", "start" ]