## `storm:latest`

```console
$ docker pull storm@sha256:a399c4382c26fbd3f4b65de1f52f5112474332ed7bb77ce4e258984dcec0fc6e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `storm:latest` - linux; amd64

```console
$ docker pull storm@sha256:5b27fff69c437903b90fe5d9f9401b3c592afe13612945fb70c3f317be9acc38
```

-	Docker Version: 17.06.2-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **150.5 MB (150469244 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b3f80b71a4b021c3c4113b139f5b273a2cd03a562c99398b130923438118d42`
-	Entrypoint: `["\/docker-entrypoint.sh"]`

```dockerfile
# Fri, 03 Nov 2017 22:10:18 GMT
ADD file:1e87ff33d1b6765b793888cd50e01b2bd0dfe152b7dbb4048008bfc2658faea7 in / 
# Fri, 03 Nov 2017 22:10:18 GMT
CMD ["/bin/sh"]
# Sat, 04 Nov 2017 05:41:40 GMT
ENV LANG=C.UTF-8
# Sat, 04 Nov 2017 05:41:40 GMT
RUN { 		echo '#!/bin/sh'; 		echo 'set -e'; 		echo; 		echo 'dirname "$(dirname "$(readlink -f "$(which javac || which java)")")"'; 	} > /usr/local/bin/docker-java-home 	&& chmod +x /usr/local/bin/docker-java-home
# Sat, 04 Nov 2017 05:50:52 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-1.8-openjdk/jre
# Sat, 04 Nov 2017 05:50:52 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/java-1.8-openjdk/jre/bin:/usr/lib/jvm/java-1.8-openjdk/bin
# Sat, 04 Nov 2017 05:50:52 GMT
ENV JAVA_VERSION=8u131
# Sat, 04 Nov 2017 05:50:53 GMT
ENV JAVA_ALPINE_VERSION=8.131.11-r2
# Sat, 04 Nov 2017 05:51:00 GMT
RUN set -x 	&& apk add --no-cache 		openjdk8-jre="$JAVA_ALPINE_VERSION" 	&& [ "$JAVA_HOME" = "$(docker-java-home)" ]
# Sat, 04 Nov 2017 16:26:04 GMT
RUN apk add --no-cache     bash     python     su-exec
# Sat, 04 Nov 2017 16:26:04 GMT
ENV STORM_USER=storm STORM_CONF_DIR=/conf STORM_DATA_DIR=/data STORM_LOG_DIR=/logs
# Sat, 04 Nov 2017 16:26:05 GMT
RUN set -x     && adduser -D "$STORM_USER"     && mkdir -p "$STORM_CONF_DIR" "$STORM_DATA_DIR" "$STORM_LOG_DIR"     && chown -R "$STORM_USER:$STORM_USER" "$STORM_CONF_DIR" "$STORM_DATA_DIR" "$STORM_LOG_DIR"
# Sat, 04 Nov 2017 16:26:05 GMT
ARG GPG_KEY=ACEFE18DD2322E1E84587A148DE03962E80B8FFD
# Sat, 04 Nov 2017 16:26:51 GMT
ARG DISTRO_NAME=apache-storm-1.1.1
# Sat, 04 Nov 2017 16:27:09 GMT
# ARGS: DISTRO_NAME=apache-storm-1.1.1 GPG_KEY=ACEFE18DD2322E1E84587A148DE03962E80B8FFD
RUN set -x     && apk add --no-cache --virtual .build-deps         gnupg     && wget -q "http://www.apache.org/dist/storm/$DISTRO_NAME/$DISTRO_NAME.tar.gz"     && wget -q "http://www.apache.org/dist/storm/$DISTRO_NAME/$DISTRO_NAME.tar.gz.asc"     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver ha.pool.sks-keyservers.net --recv-key "$GPG_KEY"     && gpg --batch --verify "$DISTRO_NAME.tar.gz.asc" "$DISTRO_NAME.tar.gz"     && tar -xzf "$DISTRO_NAME.tar.gz"     && chown -R "$STORM_USER:$STORM_USER" "$DISTRO_NAME"     && rm -rf "$GNUPGHOME" "$DISTRO_NAME.tar.gz" "$DISTRO_NAME.tar.gz.asc"     && apk del .build-deps
# Sat, 04 Nov 2017 16:27:09 GMT
WORKDIR /apache-storm-1.1.1
# Sat, 04 Nov 2017 16:27:09 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/java-1.8-openjdk/jre/bin:/usr/lib/jvm/java-1.8-openjdk/bin:/apache-storm-1.1.1/bin
# Sat, 04 Nov 2017 16:27:09 GMT
COPY file:d38c65658d07f922df720b8b043c42b170c1ac8356380e4bb8fe8934403fb0d8 in / 
# Sat, 04 Nov 2017 16:27:10 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
```

-	Layers:
	-	`sha256:b56ae66c29370df48e7377c8f9baa744a3958058a766793f821dadcb144a4647`  
		Last Modified: Wed, 25 Oct 2017 23:21:25 GMT  
		Size: 2.0 MB (1991435 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81cebc5bcaf8176775fb87f51b16c709f4c03f3848a658c9a400facb452c7cdc`  
		Last Modified: Sat, 04 Nov 2017 05:58:30 GMT  
		Size: 238.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b27fd892ecb54137910751102dfb835b185276f359a85b2ba953ce4436a4773`  
		Last Modified: Sat, 04 Nov 2017 06:04:34 GMT  
		Size: 54.3 MB (54286387 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2f132c6d5d9211039a10d2009e02cb5134f0cd53c44b59df9d1d6f6de00be9d`  
		Last Modified: Sat, 04 Nov 2017 16:27:22 GMT  
		Size: 11.5 MB (11506169 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3670e7b4f2b08b674227483dbca4fe0449065f04b2baa796fd71e34439248142`  
		Last Modified: Sat, 04 Nov 2017 16:27:19 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4aa10537024dab2c0b0195a8588a3f13cdc4bf359089fa22866b64ff1766fbb0`  
		Last Modified: Sat, 04 Nov 2017 16:28:28 GMT  
		Size: 82.7 MB (82683313 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b113c1687009056c4a687ff44a671a70259a22036be80bfe4ea20dd29239be61`  
		Last Modified: Sat, 04 Nov 2017 16:28:20 GMT  
		Size: 416.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
