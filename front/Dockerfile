FROM node:14-alpine

WORKDIR /app

COPY package*.json ./

RUN yarn install

COPY . .

# Set the backend API URL
ENV REACT_APP_API_URL=http://backend:5000

EXPOSE 3000

CMD ["yarn", "start"] 