FROM node:16-alpine

WORKDIR /app

COPY package.json package-lock.json ./

RUN npm install

COPY next.config.js ./next.config.js
COPY app ./app
COPY public ./public
COPY postcss.config.js ./postcss.config.js
COPY tailwind.config.js ./tailwind.config.js

RUN npm run build

CMD ["npm", "start"]
