FROM node:14-alpine3.11

RUN mkdir -p /app
WORKDIR /app

COPY service/dist ./service/dist
COPY package.json package-lock.json ./

# install production dependencies
RUN NODE_ENV=production npm install

ENTRYPOINT [ "npm", "run" ]
CMD [ "svc:all" ]
