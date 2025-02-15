#Imagem base
FROM node:23-alpine3.20

# Criando usuário não-root
RUN adduser -D -h /home/appuser appuser

#Diretorio de trabalho
WORKDIR /app

#Copiando os arquivos de instalações
COPY package*.json .

#Instalando as dependencias
RUN npm install

#Copiando os arquivos restantes
COPY . .

#Utilizando o usuario criado
USER appuser

#Expondo a porta padrão
EXPOSE 8080

#Rodando a aplicação
CMD [ "node", "server.js" ]
