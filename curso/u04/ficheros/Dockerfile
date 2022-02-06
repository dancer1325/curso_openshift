# Docker image with Debian and apache 2
# TODO: It doesn't finish never if you try to run it in a OS not debian. How to fix it?
FROM debian
RUN apt-get update -y && apt-get install -y \
    apache2 \
    && apt-get clean && rm -rf /var/lib/apt/lists/*
COPY ./public_html /var/www/html/
#Copy the file hosted in our machine to some folder in the container
ENTRYPOINT ["/usr/sbin/apache2ctl", "-D", "FOREGROUND"]
#ENTRYPOINT is to execute a process in the container
