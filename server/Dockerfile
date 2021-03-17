FROM node:alpine
WORKDIR /app/fibo-server
COPY package.json .
RUN npm install 
COPY ./ ./
CMD ["npm", "run", "start"]