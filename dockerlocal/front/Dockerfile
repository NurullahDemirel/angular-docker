## Build aşaması
#FROM node:18-alpine as builder
#
#WORKDIR /app
#
#COPY ../../my-angular-app/package*.json ./
#RUN npm install
#
#COPY ../../my-angular-app ./
#
#RUN npm run build --configuration=production
#
## Nginx ile servis et
#FROM nginx:alpine
#
#COPY --from=builder /app/dist/my-angular-app /usr/share/nginx/html
#
#
#EXPOSE 80
#CMD [ "-g", "daemon off;"]


FROM node:18-alpine

# Angular CLI yükle
RUN npm install -g @angular/cli

# Çalışma dizini
WORKDIR /app

# Paket dosyalarını kopyala
COPY ./package*.json ./

# Bağımlılıkları yükle
RUN npm install

# Uygulama dosyalarını kopyala
COPY . .

# 4200 portunu aç
EXPOSE 4200

# Uygulamayı başlat
CMD ["ng", "serve", "--host", "0.0.0.0"]
