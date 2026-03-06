FROM nginx:alpine

# Связываем пакет с репозиторием
LABEL org.opencontainers.image.source=https://github.com/carielflore/containers-lab-1

# Копирование конфигурации Nginx
COPY nginx.conf /etc/nginx/nginx.conf

# Копирование статических файлов
COPY index.html /usr/share/nginx/html/index.html

# Экспонирование порта
EXPOSE 80

# Запуск Nginx
CMD ["nginx", "-g", "daemon off;"]
