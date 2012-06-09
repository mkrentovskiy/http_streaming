http_streaming
==============

HTTP video streaming platform based on nginx.

1. Add nginx repo

    cd /etc/apt
    wget http://nginx.org/keys/nginx_signing.key
    apt-key add nginx_signing.key
    apt-get update

2. Build nginx

    cd /usr/src
    apt-get install git-core
    apt-get build-dep nginx
    apt-get source nginx
    git clone https://github.com/DevImpress/nginx_h264_streaming.git
    git clone https://github.com/DevImpress/OpenHttpStreamer.git
    (Replace debian/rules with this repository's file)
    apt-get -b source nginx
    dpkg -i nginx_*.deb

3. Add configuration and restart