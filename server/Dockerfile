FROM node:18-alpine
ENV NODE_ENV=production
WORKDIR /home/app

COPY . .
RUN mkdir -p home/app



RUN yarn global add @nestjs/cli@9.0.0
RUN yarn install --frozen-lockfile --production
RUN yarn build

EXPOSE 4500

ENTRYPOINT ["node", "dist/main.js"]
