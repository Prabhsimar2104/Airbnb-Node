FROM node:22-alpine

WORKDIR /app

COPY package*.json ./

RUN npm ci

COPY . .

RUN npx prisma generate --schema=src/prisma/schema.prisma

EXPOSE 3002

CMD ["npm", "start"]