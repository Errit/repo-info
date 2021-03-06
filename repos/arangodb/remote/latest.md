## `arangodb:latest`

```console
$ docker pull arangodb@sha256:39ea2e0997d37a1473d54e4b21c32ff279952782d7056a1504ec73a34a5a31eb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `arangodb:latest` - linux; amd64

```console
$ docker pull arangodb@sha256:00216123457352e8a20a38cbb4f4efe7399789f220ece5be5084c7840daefb29
```

-	Docker Version: 17.06.2-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **111.8 MB (111840062 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:045bdfb689839bd176559faaeb08426c72588743de41033d372fead5f7b74968`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["arangod"]`

```dockerfile
# Sat, 04 Nov 2017 05:26:40 GMT
ADD file:a71e077a42995a68ffe4834d85cfe26af4ea12aa8ed43decc03cc487124b1f70 in / 
# Sat, 04 Nov 2017 05:26:40 GMT
CMD ["bash"]
# Sat, 04 Nov 2017 18:07:53 GMT
MAINTAINER Frank Celler <info@arangodb.com>
# Sat, 04 Nov 2017 18:07:53 GMT
ENV ARCHITECTURE=amd64
# Sat, 04 Nov 2017 18:07:54 GMT
ENV DEB_PACKAGE_VERSION=1
# Sat, 04 Nov 2017 18:07:54 GMT
ENV ARANGO_VERSION=3.2.6
# Sat, 04 Nov 2017 18:07:54 GMT
ENV ARANGO_URL=https://download.arangodb.com/arangodb32/Debian_9.0
# Sat, 04 Nov 2017 18:07:54 GMT
ENV ARANGO_PACKAGE=arangodb3-3.2.6-1_amd64.deb
# Sat, 04 Nov 2017 18:07:54 GMT
ENV ARANGO_PACKAGE_URL=https://download.arangodb.com/arangodb32/Debian_9.0/amd64/arangodb3-3.2.6-1_amd64.deb
# Sat, 04 Nov 2017 18:07:54 GMT
ENV ARANGO_SIGNATURE_URL=https://download.arangodb.com/arangodb32/Debian_9.0/amd64/arangodb3-3.2.6-1_amd64.deb.asc
# Sat, 04 Nov 2017 18:08:02 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends gpg dirmngr     &&     rm -rf /var/lib/apt/lists/*
# Sat, 04 Nov 2017 18:08:05 GMT
RUN gpg --keyserver hkps://hkps.pool.sks-keyservers.net --recv-keys CD8CB0F1E0AD5B52E93F41E7EA93F5E56E751E9B
# Sat, 04 Nov 2017 18:08:12 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         libjemalloc1         ca-certificates         pwgen         curl     &&     rm -rf /var/lib/apt/lists/*
# Sat, 04 Nov 2017 18:10:20 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Sat, 04 Nov 2017 18:10:35 GMT
RUN curl --fail -O ${ARANGO_SIGNATURE_URL} &&           curl --fail -O ${ARANGO_PACKAGE_URL} &&             gpg --verify ${ARANGO_PACKAGE}.asc &&     (echo arangodb3 arangodb3/password password test | debconf-set-selections) &&     (echo arangodb3 arangodb3/password_again password test | debconf-set-selections) &&     DEBIAN_FRONTEND="noninteractive" dpkg -i ${ARANGO_PACKAGE} &&     rm -rf /var/lib/arangodb3/* &&     sed -ri         -e 's!127\.0\.0\.1!0.0.0.0!g'         -e 's!^(file\s*=).*!\1 -!'         -e 's!^#\s*uid\s*=.*!uid = arangodb!'         -e 's!^#\s*gid\s*=.*!gid = arangodb!'         /etc/arangodb3/arangod.conf     &&     rm -f ${ARANGO_PACKAGE}*
# Sat, 04 Nov 2017 18:10:35 GMT
VOLUME [/var/lib/arangodb3 /var/lib/arangodb3-apps]
# Sat, 04 Nov 2017 18:10:35 GMT
COPY file:bfaf23a38db232ba7808c846a5fb078a1b190c5fa005d63561e6805ab638afeb in /entrypoint.sh 
# Sat, 04 Nov 2017 18:10:36 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 04 Nov 2017 18:10:36 GMT
EXPOSE 8529/tcp
# Sat, 04 Nov 2017 18:10:36 GMT
CMD ["arangod"]
```

-	Layers:
	-	`sha256:3e17c6eae66cd23c59751c8d8f5eaf7044e0611dc5cebb12b1273be07cdac242`  
		Last Modified: Mon, 09 Oct 2017 21:41:38 GMT  
		Size: 45.1 MB (45129088 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db86fb150a4be981cd07fd83dd053a96d43fbfdd7d9858927d6d93e629e653d4`  
		Last Modified: Sat, 04 Nov 2017 18:11:18 GMT  
		Size: 6.9 MB (6920817 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d7a389f431420b95c3301f9d2df4d65d6f14a0c336a107acfeb8b83fa46b23a6`  
		Last Modified: Sat, 04 Nov 2017 18:11:16 GMT  
		Size: 3.5 KB (3466 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6631886cae3d5a1b75f234b152d4eeafa16d4fc2a61b587f34766be5ae839bf3`  
		Last Modified: Sat, 04 Nov 2017 18:11:16 GMT  
		Size: 7.4 MB (7351350 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:33a750c2bc721328b6bc20e29fa2b7ba0c01702a394f9001473d42430bfdc543`  
		Last Modified: Sat, 04 Nov 2017 18:11:15 GMT  
		Size: 115.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b0b76af7879ed55fa96ba6718084ecb605fb406d75573ed257fe00ca6c516db`  
		Last Modified: Sat, 04 Nov 2017 18:11:23 GMT  
		Size: 52.4 MB (52433396 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5bf1c0da382a084f30362d97c6bf26333a674bc0e1e22e702c563192946d283`  
		Last Modified: Sat, 04 Nov 2017 18:11:15 GMT  
		Size: 1.8 KB (1830 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
