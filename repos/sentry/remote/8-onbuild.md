## `sentry:8-onbuild`

```console
$ docker pull sentry@sha256:d990b38f11eeb6912d7b9031e417ecabc1db13b36b613ab4e690027314266b95
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `sentry:8-onbuild` - linux; amd64

```console
$ docker pull sentry@sha256:c51b2854deef05e7c0751b7206d351e87841493504862b3fe8df5bcc98b3cc31
```

-	Docker Version: 17.06.2-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **163.0 MB (162984961 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5aa176906fcb1e9b7ecf4c89c91467c345de0df7225c0cea622613018f768446`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["run","web"]`

```dockerfile
# Sat, 04 Nov 2017 05:22:35 GMT
ADD file:187fe0df97a4c52984a518a454fb7ab3984ae7b541ede7ff84dd3c5da1ce1a59 in / 
# Sat, 04 Nov 2017 05:22:36 GMT
CMD ["bash"]
# Sat, 04 Nov 2017 10:37:13 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 04 Nov 2017 10:37:13 GMT
ENV LANG=C.UTF-8
# Sat, 04 Nov 2017 14:52:10 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		libgdbm3 		libreadline6 		libsqlite3-0 		libssl1.0.0 	&& rm -rf /var/lib/apt/lists/*
# Sat, 04 Nov 2017 14:52:10 GMT
ENV GPG_KEY=C01E1CAD5EA2C4F0B8E3571504C367C218ADD4FF
# Sat, 04 Nov 2017 14:52:11 GMT
ENV PYTHON_VERSION=2.7.14
# Sat, 04 Nov 2017 14:54:34 GMT
RUN set -ex 	&& buildDeps=" 		dpkg-dev 		gcc 		libbz2-dev 		libc6-dev 		libdb-dev 		libgdbm-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tcl-dev 		tk-dev 		wget 		xz-utils 		zlib1g-dev 		$(command -v gpg > /dev/null || echo 'gnupg dirmngr') 	" 	&& apt-get update && apt-get install -y $buildDeps --no-install-recommends && rm -rf /var/lib/apt/lists/* 		&& wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz" 	&& wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc" 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$GPG_KEY" 	&& gpg --batch --verify python.tar.xz.asc python.tar.xz 	&& rm -rf "$GNUPGHOME" python.tar.xz.asc 	&& mkdir -p /usr/src/python 	&& tar -xJC /usr/src/python --strip-components=1 -f python.tar.xz 	&& rm python.tar.xz 		&& cd /usr/src/python 	&& gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 	&& ./configure 		--build="$gnuArch" 		--enable-shared 		--enable-unicode=ucs4 	&& make -j "$(nproc)" 	&& make install 	&& ldconfig 		&& apt-get purge -y --auto-remove $buildDeps 		&& find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' + 	&& rm -rf /usr/src/python
# Sat, 04 Nov 2017 14:54:34 GMT
ENV PYTHON_PIP_VERSION=9.0.1
# Sat, 04 Nov 2017 14:54:52 GMT
RUN set -ex; 		apt-get update; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 		wget -O get-pip.py 'https://bootstrap.pypa.io/get-pip.py'; 		apt-get purge -y --auto-remove wget; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		"pip==$PYTHON_PIP_VERSION" 	; 	pip --version; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' +; 	rm -f get-pip.py
# Sat, 04 Nov 2017 14:54:52 GMT
CMD ["python2"]
# Sat, 04 Nov 2017 22:13:51 GMT
RUN groupadd -r sentry && useradd -r -m -g sentry sentry
# Sat, 04 Nov 2017 22:14:21 GMT
RUN apt-get update && apt-get install -y --no-install-recommends         gcc         git         libffi-dev         libjpeg-dev         libpq-dev         libxml2-dev         libxslt-dev         libyaml-dev     && rm -rf /var/lib/apt/lists/*
# Sat, 04 Nov 2017 22:14:22 GMT
ENV PIP_NO_CACHE_DIR=off
# Sat, 04 Nov 2017 22:14:22 GMT
ENV PIP_DISABLE_PIP_VERSION_CHECK=on
# Sat, 04 Nov 2017 22:14:22 GMT
ENV GOSU_VERSION=1.10
# Sat, 04 Nov 2017 22:14:40 GMT
RUN set -x     && apt-get update && apt-get install -y --no-install-recommends wget && rm -rf /var/lib/apt/lists/*     && wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture)"     && wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture).asc"     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver ha.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4     && gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu     && rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc     && chmod +x /usr/local/bin/gosu     && gosu nobody true     && apt-get purge -y --auto-remove wget
# Sat, 04 Nov 2017 22:14:40 GMT
ENV TINI_VERSION=v0.14.0
# Sat, 04 Nov 2017 22:14:57 GMT
RUN set -x     && apt-get update && apt-get install -y --no-install-recommends wget && rm -rf /var/lib/apt/lists/*     && wget -O /usr/local/bin/tini "https://github.com/krallin/tini/releases/download/$TINI_VERSION/tini"     && wget -O /usr/local/bin/tini.asc "https://github.com/krallin/tini/releases/download/$TINI_VERSION/tini.asc"     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver ha.pool.sks-keyservers.net --recv-keys 6380DC428747F6C393FEACA59A84159D7001A4E5     && gpg --batch --verify /usr/local/bin/tini.asc /usr/local/bin/tini     && rm -r "$GNUPGHOME" /usr/local/bin/tini.asc     && chmod +x /usr/local/bin/tini     && tini -h     && apt-get purge -y --auto-remove wget
# Sat, 04 Nov 2017 22:15:22 GMT
RUN set -x     && apt-get update && apt-get install -y --no-install-recommends make && rm -rf /var/lib/apt/lists/*     && pip install librabbitmq==1.6.1     && python -c 'import librabbitmq'     && apt-get purge -y --auto-remove make
# Sat, 04 Nov 2017 22:15:22 GMT
ENV SENTRY_VERSION=8.21.0
# Sat, 04 Nov 2017 22:16:56 GMT
RUN set -x     && apt-get update && apt-get install -y --no-install-recommends wget g++ && rm -rf /var/lib/apt/lists/*     && mkdir -p /usr/src/sentry     && wget -O /usr/src/sentry/sentry-${SENTRY_VERSION}-py27-none-any.whl "https://github.com/getsentry/sentry/releases/download/${SENTRY_VERSION}/sentry-${SENTRY_VERSION}-py27-none-any.whl"     && wget -O /usr/src/sentry/sentry-${SENTRY_VERSION}-py27-none-any.whl.asc "https://github.com/getsentry/sentry/releases/download/${SENTRY_VERSION}/sentry-${SENTRY_VERSION}-py27-none-any.whl.asc"     && wget -O /usr/src/sentry/sentry_plugins-${SENTRY_VERSION}-py2.py3-none-any.whl "https://github.com/getsentry/sentry/releases/download/${SENTRY_VERSION}/sentry_plugins-${SENTRY_VERSION}-py2.py3-none-any.whl"     && wget -O /usr/src/sentry/sentry_plugins-${SENTRY_VERSION}-py2.py3-none-any.whl.asc "https://github.com/getsentry/sentry/releases/download/${SENTRY_VERSION}/sentry_plugins-${SENTRY_VERSION}-py2.py3-none-any.whl.asc"     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver ha.pool.sks-keyservers.net --recv-keys D8749766A66DD714236A932C3B2D400CE5BBCA60     && gpg --batch --verify /usr/src/sentry/sentry-${SENTRY_VERSION}-py27-none-any.whl.asc /usr/src/sentry/sentry-${SENTRY_VERSION}-py27-none-any.whl     && gpg --batch --verify /usr/src/sentry/sentry_plugins-${SENTRY_VERSION}-py2.py3-none-any.whl.asc /usr/src/sentry/sentry_plugins-${SENTRY_VERSION}-py2.py3-none-any.whl     && pip install         /usr/src/sentry/sentry-${SENTRY_VERSION}-py27-none-any.whl         /usr/src/sentry/sentry_plugins-${SENTRY_VERSION}-py2.py3-none-any.whl     && sentry --help     && sentry plugins list     && rm -r "$GNUPGHOME" /usr/src/sentry     && apt-get purge -y --auto-remove wget g++
# Sat, 04 Nov 2017 22:16:57 GMT
ENV SENTRY_CONF=/etc/sentry SENTRY_FILESTORE_DIR=/var/lib/sentry/files
# Sat, 04 Nov 2017 22:16:58 GMT
RUN mkdir -p $SENTRY_CONF && mkdir -p $SENTRY_FILESTORE_DIR
# Sat, 04 Nov 2017 22:16:58 GMT
COPY file:6b5c0c264ecaf40e9fe1838ff0926e09a661f89950c3c2b6f1612e948324733d in /etc/sentry/ 
# Sat, 04 Nov 2017 22:16:58 GMT
COPY file:d1a7cd4cbf7c842d84a135ed530ecf78f6858eaffe7f2d78824cc2906088bdd1 in /etc/sentry/ 
# Sat, 04 Nov 2017 22:16:59 GMT
COPY file:f490e4be17b442272f00cb3dac92d70a1d0164325552588b163a33fad4701f18 in /entrypoint.sh 
# Sat, 04 Nov 2017 22:16:59 GMT
EXPOSE 9000/tcp
# Sat, 04 Nov 2017 22:16:59 GMT
VOLUME [/var/lib/sentry/files]
# Sat, 04 Nov 2017 22:17:00 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 04 Nov 2017 22:17:00 GMT
CMD ["run" "web"]
# Sat, 04 Nov 2017 22:17:16 GMT
WORKDIR /usr/src/sentry
# Sat, 04 Nov 2017 22:17:16 GMT
ENV PYTHONPATH=/usr/src/sentry
# Sat, 04 Nov 2017 22:17:17 GMT
ONBUILD COPY . /usr/src/sentry
# Sat, 04 Nov 2017 22:17:17 GMT
ONBUILD RUN if [ -s requirements.txt ]; then pip install -r requirements.txt; fi
# Sat, 04 Nov 2017 22:17:17 GMT
ONBUILD RUN if [ -s setup.py ]; then pip install -e .; fi
# Sat, 04 Nov 2017 22:17:17 GMT
ONBUILD RUN if [ -s sentry.conf.py ]; then cp sentry.conf.py $SENTRY_CONF/; fi 	&& if [ -s config.yml ]; then cp config.yml $SENTRY_CONF/; fi
```

-	Layers:
	-	`sha256:d13d02fa248db2b423d6dbc8ec435675d23122f3939b5278b2156b75258e2259`  
		Last Modified: Mon, 09 Oct 2017 21:37:31 GMT  
		Size: 30.1 MB (30113318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2c103c31b601ab793ee50fe7b500cf153060996ef8cb07d46927990919eb371`  
		Last Modified: Sat, 04 Nov 2017 15:04:32 GMT  
		Size: 2.7 MB (2710531 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:33bfff8f2f5ea357fca9a460acb6d6867d8db3e2a601d810470bc6a2534496e8`  
		Last Modified: Sat, 04 Nov 2017 15:04:36 GMT  
		Size: 14.9 MB (14933702 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b66f3cbc9f3afd7ed1266d653527b49adf2c18bb72fa4506959c826df96dccc`  
		Last Modified: Sat, 04 Nov 2017 15:04:33 GMT  
		Size: 2.0 MB (1965039 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:959be65ada49d1b4bbf640d32ef70f7b6600b6300432ab43e30fd2de3f0cecf1`  
		Last Modified: Sat, 04 Nov 2017 22:17:34 GMT  
		Size: 4.4 KB (4412 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b7f3ab8e7c5071327c4d287e9132f7e2488039ffe4d18606ed7f22a1bb7cf2f`  
		Last Modified: Sat, 04 Nov 2017 22:17:44 GMT  
		Size: 53.7 MB (53658678 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1497a680abe3bcd072581d318f1d59f352dd26e95e624754d3e2f5df84a93c05`  
		Last Modified: Sat, 04 Nov 2017 22:17:33 GMT  
		Size: 844.8 KB (844810 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d5bbf570b9473a8c961c669aa35b62e61f6c5f280324f49a108d1b7d1adc94d`  
		Last Modified: Sat, 04 Nov 2017 22:17:32 GMT  
		Size: 352.1 KB (352113 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e82fb1e0f1a0a96319bc45f379a08cff4ae8a13659e12df072c1c9370d2dda30`  
		Last Modified: Sat, 04 Nov 2017 22:17:33 GMT  
		Size: 2.6 MB (2591057 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f5af1cd88968141ea2def302ad80f1d3f58d984eab17bcf8c22232c8b779e74`  
		Last Modified: Sat, 04 Nov 2017 22:17:44 GMT  
		Size: 55.8 MB (55806091 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:956f37adf70065fa4eb04f7856c434d6765a66cc5466a8969baf02805ef381ae`  
		Last Modified: Sat, 04 Nov 2017 22:17:30 GMT  
		Size: 180.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96a62ecf68ae0ebdf2e03bb82351545ac3aeaa64186ed14e975ce8796bcbebda`  
		Last Modified: Sat, 04 Nov 2017 22:17:30 GMT  
		Size: 3.4 KB (3405 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7173abb51e92139764857c70ed8931e9f019e7bd87614c2c075e63576406fb06`  
		Last Modified: Sat, 04 Nov 2017 22:17:30 GMT  
		Size: 1.1 KB (1061 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:242098e7db1f4e311e95d29f3c2c04562da01d4b91fecc690c9045c5b88a9f80`  
		Last Modified: Sat, 04 Nov 2017 22:17:30 GMT  
		Size: 426.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39494c4d9c5c78d4253b42ea11940782c94599afffe88091feb5d8131aa3bb47`  
		Last Modified: Sat, 04 Nov 2017 22:18:13 GMT  
		Size: 138.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
