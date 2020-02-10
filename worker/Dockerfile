FROM node:alpine

WORKDIR '/app'
COPY ./package.json ./
RUN npm install
COPY . .

# This is used for develop, change to start when to production
# CMD ["npm", "run", "dev"]
# This is also a reflect of package.json
CMD ["npm", "run", "start"]
