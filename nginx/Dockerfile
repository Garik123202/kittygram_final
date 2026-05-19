FROM nginx:1.22.1

# Удаляем шаблоны, чтобы Nginx не перезаписывал конфиг
RUN rm -rf /etc/nginx/templates/*

# Копируем конфиг сразу в conf.d (не как шаблон!)
COPY nginx.conf /etc/nginx/conf.d/default.conf
