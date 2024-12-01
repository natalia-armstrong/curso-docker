FROM node:16-alpine
WORKDIR /app
COPY package.json .
RUN apk add --no-cache python3 g++ make
RUN yarn install --production
COPY . .
CMD ["node", "scr/index.js"]
EXPOSE 3000