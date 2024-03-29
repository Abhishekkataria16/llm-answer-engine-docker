FROM node:lts-alpine3.19
WORKDIR /app
COPY . /app
RUN npm install -g npm@latest && npm install --legacy-peer-deps
RUN npx next telemetry disable
EXPOSE 3000
ENTRYPOINT ["npm", "run", "dev"] 
