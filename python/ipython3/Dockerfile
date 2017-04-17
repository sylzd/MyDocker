FROM daocloud.io/python:3-onbuild

MAINTAINER sylzd <sylzd@whu.edu.cn>


RUN mkdir -p /app
WORKDIR /app
ADD requirements.txt requirements.txt
RUN pip install -r requirements.txt -i https://pypi.douban.com/simple
COPY docker-entrypoint.sh /bin/

# transmmit dos file to unix file
RUN cat -v /bin/docker-entrypoint.sh
RUN cat /bin/docker-entrypoint.sh | tr -d "\r" > /bin/docker-entrypoint.sh
RUN cat -v /bin/docker-entrypoint.sh
# view packages
RUN ls /usr/local/bin
RUN chmod +x /bin/docker-entrypoint.sh
EXPOSE 8888
ENTRYPOINT ["/bin/docker-entrypoint.sh"]
CMD [""]