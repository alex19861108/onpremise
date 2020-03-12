ARG BASE_IMAGE
FROM ${BASE_IMAGE}
#COPY sources.list /etc/apt/sources.list
#RUN sed -i 's@deb.debian.org@mirrors.aliyun.com@g' /etc/apt/sources.list
RUN cat /etc/os-release
RUN apt-get update && apt-get install -y --no-install-recommends cron && \
    rm -r /var/lib/apt/lists/*
COPY entrypoint.sh /entrypoint.sh
ENTRYPOINT ["/entrypoint.sh"]
