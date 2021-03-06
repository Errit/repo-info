## `telegraf:alpine`

```console
$ docker pull telegraf@sha256:d90b183a9edd4ffcb339c5091c2d36e96f444ad4345f723565a4045491f8f208
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `telegraf:alpine` - linux; amd64

```console
$ docker pull telegraf@sha256:ff4dc1e74861b7138cae4d47c5d79b33347b36f849ef4354b9f552ba5e1ca070
```

-	Docker Version: 17.06.2-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.6 MB (12617362 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8ffae445f54f280cb6033356ec888b80424a8a92d31ddca904046953cee25370`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Fri, 03 Nov 2017 22:10:27 GMT
ADD file:92bfed3f8dfbee01eab85c6a1d6bc6894c5a75f9a4e2c414e9b4d05b9fcd19d0 in / 
# Fri, 03 Nov 2017 22:10:27 GMT
CMD ["/bin/sh"]
# Fri, 03 Nov 2017 22:17:49 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Sat, 04 Nov 2017 09:47:56 GMT
RUN apk add --no-cache iputils ca-certificates net-snmp-tools &&     update-ca-certificates
# Sat, 04 Nov 2017 09:48:31 GMT
ENV TELEGRAF_VERSION=1.4.3
# Sat, 04 Nov 2017 09:48:42 GMT
RUN set -ex &&     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done &&     wget -q https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}-static_linux_amd64.tar.gz.asc &&     wget -q https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}-static_linux_amd64.tar.gz &&     gpg --batch --verify telegraf-${TELEGRAF_VERSION}-static_linux_amd64.tar.gz.asc telegraf-${TELEGRAF_VERSION}-static_linux_amd64.tar.gz &&     mkdir -p /usr/src /etc/telegraf &&     tar -C /usr/src -xzf telegraf-${TELEGRAF_VERSION}-static_linux_amd64.tar.gz &&     mv /usr/src/telegraf*/telegraf.conf /etc/telegraf/ &&     chmod +x /usr/src/telegraf*/* &&     cp -a /usr/src/telegraf*/* /usr/bin/ &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps
# Sat, 04 Nov 2017 09:48:43 GMT
EXPOSE 8092/udp 8094/tcp 8125/udp
# Sat, 04 Nov 2017 09:48:43 GMT
COPY file:43e6828e001b57ab465cff8dfd3d30830289afe7ca5944b61641956bfe38cd1c in /entrypoint.sh 
# Sat, 04 Nov 2017 09:48:43 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 04 Nov 2017 09:48:43 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:b1f00a6a160cd3696edba6f13ebd1d6a5808216a78ec4b753444ab8f30483b1f`  
		Last Modified: Wed, 25 Oct 2017 23:22:48 GMT  
		Size: 2.0 MB (1970236 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:309c3337f4743db6a36cc534b3703bfd713e510d2f5a542abb5ffb963560e053`  
		Last Modified: Fri, 03 Nov 2017 22:19:06 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07eb27f708d43b6827dc9105b43541d5d4c930e4523fcd093a300ca4d759d824`  
		Last Modified: Sat, 04 Nov 2017 09:49:15 GMT  
		Size: 1.8 MB (1771320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07fcfb20d0551a24889e95f69cddab03fcee6b36442b6c054e30adec0e514043`  
		Last Modified: Sat, 04 Nov 2017 09:49:56 GMT  
		Size: 8.9 MB (8875469 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d6e618f50a3aff23a6789b6f7ae31af0b37a4cd0a30e24ab8e391c79ba6fcde`  
		Last Modified: Sat, 04 Nov 2017 09:49:53 GMT  
		Size: 184.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
