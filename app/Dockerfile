FROM node:16-alpine

# Diretório de trabalho dentro do contêiner
WORKDIR /app

# Copiar o package.json e yarn.lock para o contêiner
COPY package.json . 

# Instalar dependências do sistema para compilar sqlite3
RUN apk add --no-cache python3 g++ make sqlite-dev

# Instalar dependências com yarn
RUN yarn install --production

# Copiar o restante do código da aplicação para dentro do contêiner
COPY . .

# Rodar a aplicação Node.js
CMD ["node", "src/index.js"]

# Expor a porta 3000
EXPOSE 3000