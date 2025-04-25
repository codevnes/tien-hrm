FROM node:14-alpine

WORKDIR /app

COPY package*.json ./

RUN yarn install

COPY . .

# Update database configuration
RUN sed -i 's/host: "localhost"/host: "db"/' ./src/utils/Database.js
RUN sed -i 's/password: ""/password: "root_password"/' ./src/utils/Database.js
RUN sed -i 's/database: "database name"/database: "pos"/' ./src/utils/Database.js

EXPOSE 5000

CMD ["yarn", "start"] 