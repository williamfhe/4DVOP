FROM ubuntu:16.04

RUN apt-get update && \
  apt-get install -y --no-install-recommends \
  wget ca-certificates && \
  apt-get clean && \
  rm -rf /var/lib/apt/lists/*

WORKDIR /plex

RUN wget -O /tmp/plex.deb https://downloads.plex.tv/plex-media-server-new/1.18.7.2457-77cb9455c/debian/plexmediaserver_1.18.7.2457-77cb9455c_amd64.deb && \
  dpkg -i /tmp/plex.deb


CMD ["/usr/sbin/start_pms"]