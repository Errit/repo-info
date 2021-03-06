## `mysql:latest`

```console
$ docker pull mysql@sha256:1a2f9361228e9b10b4c77a651b460828514845dc7ac51735b919c2c4aec864b7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `mysql:latest` - linux; amd64

```console
$ docker pull mysql@sha256:a0423a7d021b7a7775f1d2db1014bd15fde029f538c1f8d97c9832aa4a25209f
```

-	Docker Version: 17.06.2-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **144.2 MB (144191461 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5709795eeffac51eca46cf40ab36669aad27e8cb4b0e91876d5e9f7bafad6acb`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Sat, 04 Nov 2017 05:21:35 GMT
ADD file:55b071e2cfc3ea2f4bbf048d7d676e3c06a77a9a98d63f7af291f3decb495ec8 in / 
# Sat, 04 Nov 2017 05:21:36 GMT
CMD ["bash"]
# Sat, 04 Nov 2017 05:33:35 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Sat, 04 Nov 2017 05:33:36 GMT
ENV GOSU_VERSION=1.7
# Sat, 04 Nov 2017 05:33:58 GMT
RUN set -x 	&& apt-get update && apt-get install -y --no-install-recommends ca-certificates wget && rm -rf /var/lib/apt/lists/* 	&& wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture)" 	&& wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture).asc" 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --keyserver ha.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4 	&& gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu 	&& rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc 	&& chmod +x /usr/local/bin/gosu 	&& gosu nobody true 	&& apt-get purge -y --auto-remove ca-certificates wget
# Sat, 04 Nov 2017 05:33:58 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Sat, 04 Nov 2017 14:11:16 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		pwgen 		openssl 		perl 	&& rm -rf /var/lib/apt/lists/*
# Sat, 04 Nov 2017 14:11:20 GMT
RUN set -ex; 	key='A4A9406876FCBD3C456770C88C718D3B5072E1F5'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	gpg --export "$key" > /etc/apt/trusted.gpg.d/mysql.gpg; 	rm -r "$GNUPGHOME"; 	apt-key list > /dev/null
# Sat, 04 Nov 2017 14:11:41 GMT
ENV MYSQL_MAJOR=5.7
# Sat, 04 Nov 2017 14:11:41 GMT
ENV MYSQL_VERSION=5.7.20-1debian8
# Sat, 04 Nov 2017 14:11:42 GMT
RUN echo "deb http://repo.mysql.com/apt/debian/ jessie mysql-${MYSQL_MAJOR}" > /etc/apt/sources.list.d/mysql.list
# Sat, 04 Nov 2017 14:12:05 GMT
RUN { 		echo mysql-community-server mysql-community-server/data-dir select ''; 		echo mysql-community-server mysql-community-server/root-pass password ''; 		echo mysql-community-server mysql-community-server/re-root-pass password ''; 		echo mysql-community-server mysql-community-server/remove-test-db select false; 	} | debconf-set-selections 	&& apt-get update && apt-get install -y mysql-server="${MYSQL_VERSION}" && rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mysql && mkdir -p /var/lib/mysql /var/run/mysqld 	&& chown -R mysql:mysql /var/lib/mysql /var/run/mysqld 	&& chmod 777 /var/run/mysqld 	&& find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log)/#&/' 	&& echo '[mysqld]\nskip-host-cache\nskip-name-resolve' > /etc/mysql/conf.d/docker.cnf
# Sat, 04 Nov 2017 14:12:06 GMT
VOLUME [/var/lib/mysql]
# Sat, 04 Nov 2017 14:12:06 GMT
COPY file:5453fdbdb142b28e9aa4df64d5e1f42a740f018457cb1c65d113b947858ae314 in /usr/local/bin/ 
# Sat, 04 Nov 2017 14:12:07 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Sat, 04 Nov 2017 14:12:07 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 04 Nov 2017 14:12:07 GMT
EXPOSE 3306/tcp
# Sat, 04 Nov 2017 14:12:07 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:85b1f47fba49da65256f07c8790542a3880e9216f9c491965040f35ce2c6ca7a`  
		Last Modified: Mon, 09 Oct 2017 21:36:40 GMT  
		Size: 52.6 MB (52595124 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5671503d4f93a519cf211982c698f0185372a3818c88ae153fecccebccb02d2c`  
		Last Modified: Sat, 04 Nov 2017 05:36:46 GMT  
		Size: 2.1 KB (2090 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b43b3b913cbf2bc760d865112caa9e70367bb9f477607a162806f6fe4bfc0c1`  
		Last Modified: Sat, 04 Nov 2017 05:36:44 GMT  
		Size: 1.3 MB (1302926 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4fbb803665d088eae212e9dcb44046766737a360e6bdcd560fa6c608516709d0`  
		Last Modified: Sat, 04 Nov 2017 05:36:43 GMT  
		Size: 115.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05808866e6f9aa32dd0d90e8ddf2fa61f0aadf1ea3a6cd241e4d8560599730e5`  
		Last Modified: Sat, 04 Nov 2017 14:14:25 GMT  
		Size: 10.7 MB (10711104 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d8c65d48cfafbaa45aa6fee3838f34839e3f1a15a6fe3e6279106876480f971`  
		Last Modified: Sat, 04 Nov 2017 14:14:22 GMT  
		Size: 20.1 KB (20087 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e189e187b2b50cee94b84c7ba30e897f70a6bc9edd5f6f4b13c1e2c86834cf93`  
		Last Modified: Sat, 04 Nov 2017 14:14:49 GMT  
		Size: 221.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:02d3e6011ee86731c6442c2989f3dbe0ca0fa32e2d3d2cb4298655e60e105023`  
		Last Modified: Sat, 04 Nov 2017 14:15:01 GMT  
		Size: 79.6 MB (79556940 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d43b32d5ce043b6cbbbbae384ae8e2a34f3ee1264676e3e1f23201bcf1e6a99a`  
		Last Modified: Sat, 04 Nov 2017 14:14:49 GMT  
		Size: 2.7 KB (2733 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a809168ab453ee345099ca10ee1914ecd855151127c2ecf00be4b645119c034`  
		Last Modified: Sat, 04 Nov 2017 14:14:49 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
