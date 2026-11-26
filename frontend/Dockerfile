# Etapa 1: Build do Angular (mantém Node)
FROM node:22-alpine AS build

WORKDIR /app
COPY package*.json ./
RUN npm install
COPY . .
RUN npm run build

# Etapa 2: Servidor Bun
FROM oven/bun:1-alpine

WORKDIR /app

# Copia os arquivos compilados
COPY --from=build /app/dist/*/browser ./dist
COPY server.js ./

USER bun
EXPOSE 3000

CMD ["bun", "server.js"]   