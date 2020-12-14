FROM 10.47.164.49:443/docker-local/node

WORKDIR /app

RUN apt update \
  && apt upgrade -y \
  && npm install -g nodemon

COPY package*.json ./

RUN npm ci \
 && npm cache clean --force 
# && mv /app/node_modules /node_modules

#COPY . .

ENV PORT 80

EXPOSE 80

CMD ["node", "server.js"]
