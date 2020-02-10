FROM node:alpine as builder
WORKDIR '/app'
COPY ./package.json ./
RUN npm install
COPY . .
RUN npm run build

FROM nginx
EXPOSE 3000
COPY ./nginx/default.conf /etc/nginx/conf.d/default.conf

# copy from above built image
# /app/build is the default folder for all production version of above 
COPY --from=builder /app/build /usr/share/nginx/html


