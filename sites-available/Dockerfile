FROM nginx:latest
RUN apt-get update \
    && apt-get install -y vim less
RUN mkdir -p /etc/nginx/sites-available/
RUN mkdir -p /etc/nginx/sites-enabled/
RUN ln -nfs /etc/nginx/sites-available/hoge.example.com.conf /etc/nginx/sites-enabled/
RUN ln -nfs /etc/nginx/sites-available/fuga.example.com.conf /etc/nginx/sites-enabled/
RUN mkdir -p /var/www/hoge/html
RUN mkdir -p /var/www/fuga/html
RUN chown -R $USER:$USER /var/www/hoge/html
RUN chown -R $USER:$USER /var/www/fuga/html
RUN chmod -R 755 /var/www/hoge/html
RUN chmod -R 755 /var/www/fuga/html
RUN touch /var/www/hoge/html/index.html && echo 'hoge' >> /var/www/hoge/html/index.html
RUN touch /var/www/fuga/html/index.html && echo 'fuga' >> /var/www/fuga/html/index.html