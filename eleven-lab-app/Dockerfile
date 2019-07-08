FROM node:12.6.0-alpine

RUN mkdir -p /usr/app/eleven-lab-app
WORKDIR /usr/app/eleven-lab-app

# Install dependencies
COPY package*.json ./
COPY yarn.lock .
RUN yarn install

# Bundle app source
COPY . /usr/app/eleven-lab-app

# Exports
EXPOSE 4000
CMD ["yarn", "run", "start"]