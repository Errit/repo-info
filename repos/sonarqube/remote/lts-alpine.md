## `sonarqube:lts-alpine`

```console
$ docker pull sonarqube@sha256:e8f7813c62f7309e6959d05e2f2e4f99bfc242c52aaf44b9b1996fc7181be6d6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `sonarqube:lts-alpine` - linux; amd64

```console
$ docker pull sonarqube@sha256:e32a55f34d7f3f4573c289c941e41c6853b8a78e89f20a7f22ac19b435f35038
```

-	Docker Version: 17.06.2-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **194.5 MB (194532319 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1d7a4c28b94bf08d94d45788974f9fc8fad5ec711e4746082838091bd69ef7e0`
-	Entrypoint: `[".\/bin\/run.sh"]`

```dockerfile
# Fri, 03 Nov 2017 22:10:18 GMT
ADD file:1e87ff33d1b6765b793888cd50e01b2bd0dfe152b7dbb4048008bfc2658faea7 in / 
# Fri, 03 Nov 2017 22:10:18 GMT
CMD ["/bin/sh"]
# Sat, 04 Nov 2017 05:41:40 GMT
ENV LANG=C.UTF-8
# Sat, 04 Nov 2017 05:41:40 GMT
RUN { 		echo '#!/bin/sh'; 		echo 'set -e'; 		echo; 		echo 'dirname "$(dirname "$(readlink -f "$(which javac || which java)")")"'; 	} > /usr/local/bin/docker-java-home 	&& chmod +x /usr/local/bin/docker-java-home
# Sat, 04 Nov 2017 05:48:22 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-1.8-openjdk
# Sat, 04 Nov 2017 05:48:22 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/java-1.8-openjdk/jre/bin:/usr/lib/jvm/java-1.8-openjdk/bin
# Sat, 04 Nov 2017 05:48:22 GMT
ENV JAVA_VERSION=8u131
# Sat, 04 Nov 2017 05:48:22 GMT
ENV JAVA_ALPINE_VERSION=8.131.11-r2
# Sat, 04 Nov 2017 05:48:29 GMT
RUN set -x 	&& apk add --no-cache 		openjdk8="$JAVA_ALPINE_VERSION" 	&& [ "$JAVA_HOME" = "$(docker-java-home)" ]
# Sat, 04 Nov 2017 09:00:19 GMT
ENV SONAR_VERSION=5.6.7 SONARQUBE_HOME=/opt/sonarqube SONARQUBE_JDBC_USERNAME=sonar SONARQUBE_JDBC_PASSWORD=sonar SONARQUBE_JDBC_URL=
# Sat, 04 Nov 2017 09:00:19 GMT
EXPOSE 9000/tcp
# Sat, 04 Nov 2017 09:00:20 GMT
RUN addgroup -S sonarqube && adduser -S -G sonarqube sonarqube
# Sat, 04 Nov 2017 09:00:41 GMT
RUN set -x     && apk add --no-cache gnupg unzip     && apk add --no-cache libressl wget     && apk add --no-cache su-exec     && apk add --no-cache bash     && gpg --keyserver ha.pool.sks-keyservers.net --recv-keys F1182E81C792928921DBCAB4CFCA4A29D26468DE     && mkdir /opt     && cd /opt     && wget -O sonarqube.zip --no-verbose https://sonarsource.bintray.com/Distribution/sonarqube/sonarqube-$SONAR_VERSION.zip     && wget -O sonarqube.zip.asc --no-verbose https://sonarsource.bintray.com/Distribution/sonarqube/sonarqube-$SONAR_VERSION.zip.asc     && gpg --batch --verify sonarqube.zip.asc sonarqube.zip     && unzip sonarqube.zip     && mv sonarqube-$SONAR_VERSION sonarqube     && chown -R sonarqube:sonarqube sonarqube     && rm sonarqube.zip*     && rm -rf $SONARQUBE_HOME/bin/*
# Sat, 04 Nov 2017 09:00:41 GMT
VOLUME [/opt/sonarqube/data]
# Sat, 04 Nov 2017 09:00:41 GMT
WORKDIR /opt/sonarqube
# Sat, 04 Nov 2017 09:00:42 GMT
COPY file:b692f3c4a910c6cabb33643ad789b4e104de43e0b26bf76e018578d0a457f0b3 in /opt/sonarqube/bin/ 
# Sat, 04 Nov 2017 09:00:42 GMT
ENTRYPOINT ["./bin/run.sh"]
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
	-	`sha256:9f7678525069841024e8702b5d9dbc066f2c8970afee9c11248f7af18c147ec3`  
		Last Modified: Sat, 04 Nov 2017 06:02:25 GMT  
		Size: 70.1 MB (70053766 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9979f135d4aba6a6e830932348f7884f16a5b7adeb53a64a58905d2fd06f84b5`  
		Last Modified: Sat, 04 Nov 2017 09:02:49 GMT  
		Size: 1.3 KB (1257 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69f5e8509c625220122ee6ab8ad4e3c87d140c1a292ee4898e82bbfeaeacabbd`  
		Last Modified: Sat, 04 Nov 2017 09:02:57 GMT  
		Size: 122.5 MB (122485142 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b5022623c06f90388406097cb39c7b9a69dc04cbd77a3e6b18ed021b97ee6404`  
		Last Modified: Sat, 04 Nov 2017 09:02:49 GMT  
		Size: 481.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
