FROM node:16

WORKDIR /app/src/frontend

COPY . /app/src/frontend

RUN npm install -g npm@latest && \
    npm install

EXPOSE 3000

CMD ["npm", "start"]