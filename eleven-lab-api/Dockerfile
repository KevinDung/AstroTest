FROM node:12.6.0-alpine

RUN mkdir -p /usr/app/eleven-lab-api
WORKDIR /usr/app/eleven-lab-api

# Install dependencies
COPY package*.json ./
COPY yarn.lock .
RUN yarn install

# Bundle app source
COPY . /usr/app/eleven-lab-api

# Exports
EXPOSE 3000
CMD ["yarn", "run", "start"]
