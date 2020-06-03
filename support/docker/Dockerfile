FROM kuborgh/php-5.2

ADD https://nl.wordpress.org/wordpress-5.0.9-nl_NL.tar.gz /opt/

RUN mkdir /project
RUN tar -xzf /opt/wordpress-5.0.9-nl_NL.tar.gz -C /project/ --strip-components=1
RUN rm -rf /opt/wordpress-5.0.9-nl_NL.tar.gz

WORKDIR /project

VOLUME /project

EXPOSE 80