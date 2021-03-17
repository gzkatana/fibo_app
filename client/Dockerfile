FROM node:alpine as builder
WORKDIR FROM node:alpine
WORKDIR /app/fibo-client
COPY package.json .
RUN npm install 
COPY ./ ./
CMD ["npm", "run", "start"]
COPY package.json .
RUN npm install 
COPY ./ ./
RUN npm run build

FROM nginx
EXPOSE 3000
COPY ./nginx/default.conf /etc/nginx/conf.d/default.conf
COPY --from=builder /app/fibo-client/build /usr/share/nginx/html




