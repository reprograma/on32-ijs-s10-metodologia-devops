FROM node:18

WORKDIR /app

# Copie o package.json e o package-lock.json para o diretório de trabalho
COPY package*.json ./

# Instale as dependências do projeto
RUN npm ci

# Copie o restante dos arquivos da aplicação para o diretório de trabalho
COPY . .

# Compile a aplicação TypeScript
RUN npm run build

# Exponha a porta que a aplicação usará (ajuste conforme necessário)
EXPOSE 3000

# Comando para rodar a aplicação
CMD ["npm", "start"]
