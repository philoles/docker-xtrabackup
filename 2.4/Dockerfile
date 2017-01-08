FROM debian:jessie

RUN \
    echo "deb http://repo.percona.com/apt jessie main" > /etc/apt/sources.list.d/percona.list \
    && echo "deb-src http://repo.percona.com/apt jessie main" >> /etc/apt/sources.list.d/percona.list \
    && apt-key adv --keyserver ha.pool.sks-keyservers.net --recv-keys 1C4CBDCDCD2EFD2A

RUN \
   apt-get update && apt-get install -y --no-install-recommends \
      percona-xtrabackup-24 \
      percona-toolkit \
      qpress \
   && rm -rf /var/lib/apt/lists/* \

CMD ["bash"]
