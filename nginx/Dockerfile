FROM nginx:alpine

# Копирование конфигурации Nginx
COPY nginx.conf /etc/nginx/nginx.conf

# Копирование статических файлов
COPY index.html /usr/share/nginx/html/index.html

# Экспонирование порта
EXPOSE 80

# Запуск Nginx
CMD ["nginx", "-g", "daemon off;"]
