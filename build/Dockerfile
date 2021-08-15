FROM node:12 AS build

WORKDIR /app

COPY package.json ./
RUN npm install
COPY . ./
RUN npm run build

FROM nginx:1.19-alpine as prod
COPY --from=build /app/public /usr/share/nginx/html

FROM build as debug
ENV HOST=0.0.0.0
EXPOSE 5000
CMD ["npm" ,"run", "dev"]

#RUN npm install -g nodemon

#EXPOSE 5000
#ENV HOST=0.0.0.0
#CMD ["nodemon","--inspect=0.0.0.0:5000","./src/main.js"]

#FROM nginx:1.19-alpine
#COPY --from=build /app/public /usr/share/nginx/html