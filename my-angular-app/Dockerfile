FROM node:18-alpine

# Angular CLI yükle
RUN npm install -g @angular/cli

# Çalışma dizini
WORKDIR /app

# Paket dosyalarını kopyala
COPY package*.json ./

# Bağımlılıkları yükle
RUN npm install

# Uygulama dosyalarını kopyala
COPY . .

# 4200 portunu aç
EXPOSE 4200

# Uygulamayı başlat
CMD ["ng", "serve", "--host", "0.0.0.0"]
