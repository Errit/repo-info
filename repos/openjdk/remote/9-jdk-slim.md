## `openjdk:9-jdk-slim`

```console
$ docker pull openjdk@sha256:282ea1ab5fedb55ab798b3610a4e00760a93c2d0283aa21999cd4a88c1455b74
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v5
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le
	-	linux; s390x

### `openjdk:9-jdk-slim` - linux; amd64

```console
$ docker pull openjdk@sha256:d1207f65587e95ec9366810e37eb73c1129afc52a59ec6b726d6d9e1ea53c3c0
```

-	Docker Version: 17.06.2-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **182.5 MB (182477795 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6a894dcdb2e6689480a0cbc321bf6b7e479111b6f6615fa78b78f770e1dfe880`
-	Default Command: `["jshell"]`

```dockerfile
# Sat, 04 Nov 2017 05:26:16 GMT
ADD file:4f5c99023af857b40a8bb5ef610e4fc8a4ab4bcec326fcffddd3c18162eb5a90 in / 
# Sat, 04 Nov 2017 05:26:16 GMT
CMD ["bash"]
# Sat, 04 Nov 2017 05:52:46 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 	&& rm -rf /var/lib/apt/lists/*
# Sat, 04 Nov 2017 05:52:46 GMT
ENV LANG=C.UTF-8
# Sat, 04 Nov 2017 05:52:47 GMT
RUN { 		echo '#!/bin/sh'; 		echo 'set -e'; 		echo; 		echo 'dirname "$(dirname "$(readlink -f "$(which javac || which java)")")"'; 	} > /usr/local/bin/docker-java-home 	&& chmod +x /usr/local/bin/docker-java-home
# Sat, 04 Nov 2017 05:52:48 GMT
RUN ln -svT "/usr/lib/jvm/java-9-openjdk-$(dpkg --print-architecture)" /docker-java-home
# Sat, 04 Nov 2017 05:52:48 GMT
ENV JAVA_HOME=/docker-java-home
# Sat, 04 Nov 2017 05:52:48 GMT
ENV JAVA_VERSION=9.0.1+11
# Sat, 04 Nov 2017 05:52:48 GMT
ENV JAVA_DEBIAN_VERSION=9.0.1+11-1
# Sat, 04 Nov 2017 05:53:24 GMT
RUN set -ex; 		if [ ! -d /usr/share/man/man1 ]; then 		mkdir -p /usr/share/man/man1; 	fi; 		apt-get update; 	apt-get install -y 		openjdk-9-jdk-headless="$JAVA_DEBIAN_VERSION" 	; 	rm -rf /var/lib/apt/lists/*; 		[ "$(readlink -f "$JAVA_HOME")" = "$(docker-java-home)" ]; 		update-alternatives --get-selections | awk -v home="$(readlink -f "$JAVA_HOME")" 'index($3, home) == 1 { $2 = "manual"; print | "update-alternatives --set-selections" }'; 	update-alternatives --query java | grep -q 'Status: manual'
# Sat, 04 Nov 2017 05:53:24 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:3f84388a33351f025313af89e330691da0d2d0f7309fa0d0f6cbb15e0160473d`  
		Last Modified: Mon, 09 Oct 2017 21:40:21 GMT  
		Size: 24.9 MB (24897397 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb2a453fe79fc30d4f012fe130ad4f023aa3a345cb5ca95f379c325ab7c99ae7`  
		Last Modified: Sat, 04 Nov 2017 06:06:11 GMT  
		Size: 460.4 KB (460376 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3685d649c8ca827bf516114bca2ed6146e79ee2f7a91a9fcc332e41c60ea040`  
		Last Modified: Sat, 04 Nov 2017 06:06:10 GMT  
		Size: 248.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6394d7fced41f1e1b9e48654146516aaeec2d32cb66d0023baeca5eef6c7fd64`  
		Last Modified: Sat, 04 Nov 2017 06:06:10 GMT  
		Size: 131.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3ac603ce5cd75c2326d8e53f8c9b53f9238466e7280fc1a971a2a124ed4dddd`  
		Last Modified: Sat, 04 Nov 2017 06:06:38 GMT  
		Size: 157.1 MB (157119643 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `openjdk:9-jdk-slim` - linux; arm variant v5

```console
$ docker pull openjdk@sha256:44beeb6a3c98287105fcd0ad50e03f9bc1cfa7ac9e8d6e437ede2e9720e465cc
```

-	Docker Version: 17.06.0-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **155.3 MB (155257490 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0c92b201ad8f46dffee606246c2750a4660bdd34e481960dc51635b18d877d5c`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 09 Oct 2017 21:43:49 GMT
ADD file:53515d12c277346acef474e8405d99646f72a11380a3b75d1dad8756510e6870 in / 
# Mon, 09 Oct 2017 21:43:49 GMT
CMD ["bash"]
# Mon, 09 Oct 2017 22:30:34 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 	&& rm -rf /var/lib/apt/lists/*
# Mon, 09 Oct 2017 22:30:35 GMT
ENV LANG=C.UTF-8
# Mon, 09 Oct 2017 22:30:36 GMT
RUN { 		echo '#!/bin/sh'; 		echo 'set -e'; 		echo; 		echo 'dirname "$(dirname "$(readlink -f "$(which javac || which java)")")"'; 	} > /usr/local/bin/docker-java-home 	&& chmod +x /usr/local/bin/docker-java-home
# Mon, 09 Oct 2017 22:30:37 GMT
RUN ln -svT "/usr/lib/jvm/java-9-openjdk-$(dpkg --print-architecture)" /docker-java-home
# Mon, 09 Oct 2017 22:30:38 GMT
ENV JAVA_HOME=/docker-java-home
# Sat, 04 Nov 2017 10:03:28 GMT
ENV JAVA_VERSION=9.0.1+11
# Sat, 04 Nov 2017 10:03:28 GMT
ENV JAVA_DEBIAN_VERSION=9.0.1+11-1
# Sat, 04 Nov 2017 10:04:20 GMT
RUN set -ex; 		if [ ! -d /usr/share/man/man1 ]; then 		mkdir -p /usr/share/man/man1; 	fi; 		apt-get update; 	apt-get install -y 		openjdk-9-jdk-headless="$JAVA_DEBIAN_VERSION" 	; 	rm -rf /var/lib/apt/lists/*; 		[ "$(readlink -f "$JAVA_HOME")" = "$(docker-java-home)" ]; 		update-alternatives --get-selections | awk -v home="$(readlink -f "$JAVA_HOME")" 'index($3, home) == 1 { $2 = "manual"; print | "update-alternatives --set-selections" }'; 	update-alternatives --query java | grep -q 'Status: manual'
# Sat, 04 Nov 2017 10:04:21 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:ea37965471e13f9e6050ef152f0f00007063aed293f9ab9254f7ae0062caffe9`  
		Last Modified: Mon, 09 Oct 2017 21:49:34 GMT  
		Size: 23.3 MB (23348454 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ec082c0f8a485cb2fc949ff337b67626da849d056263c1e0248f98c847b5c21`  
		Last Modified: Mon, 09 Oct 2017 22:35:30 GMT  
		Size: 453.8 KB (453840 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56f6cc6201a4bb264d660ccd911867d17fbe817ca21b715fc9434b49ebed1a78`  
		Last Modified: Mon, 09 Oct 2017 22:35:30 GMT  
		Size: 247.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a147ee1897b6272956335a08816ffbef1187d77ddafd822f9312e36e7034eb1d`  
		Last Modified: Mon, 09 Oct 2017 22:35:30 GMT  
		Size: 132.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f29dab03626fc0d33c937c1de2fa3d8c443ac4b00ece6284473d8c5511184b4d`  
		Last Modified: Sat, 04 Nov 2017 10:13:27 GMT  
		Size: 131.5 MB (131454817 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `openjdk:9-jdk-slim` - linux; arm variant v7

```console
$ docker pull openjdk@sha256:d46b1a6733857b3d6bfb2f683f7272ac5548044037f70d5581de153f977e7843
```

-	Docker Version: 17.06.0-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **158.9 MB (158878610 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e607a104ab924b128e31e8c807024e14716c0c6c80301a83f16a7ab18d17c457`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 09 Oct 2017 21:44:28 GMT
ADD file:5d5c4a7233c6c9a2682e39e732a1f23db741e074dbc5b6f16309bb53d0bdaf18 in / 
# Mon, 09 Oct 2017 21:44:29 GMT
CMD ["bash"]
# Mon, 09 Oct 2017 23:10:27 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 	&& rm -rf /var/lib/apt/lists/*
# Mon, 09 Oct 2017 23:10:27 GMT
ENV LANG=C.UTF-8
# Mon, 09 Oct 2017 23:10:29 GMT
RUN { 		echo '#!/bin/sh'; 		echo 'set -e'; 		echo; 		echo 'dirname "$(dirname "$(readlink -f "$(which javac || which java)")")"'; 	} > /usr/local/bin/docker-java-home 	&& chmod +x /usr/local/bin/docker-java-home
# Mon, 09 Oct 2017 23:10:30 GMT
RUN ln -svT "/usr/lib/jvm/java-9-openjdk-$(dpkg --print-architecture)" /docker-java-home
# Mon, 09 Oct 2017 23:10:30 GMT
ENV JAVA_HOME=/docker-java-home
# Sat, 04 Nov 2017 01:31:01 GMT
ENV JAVA_VERSION=9.0.1+11
# Sat, 04 Nov 2017 01:31:01 GMT
ENV JAVA_DEBIAN_VERSION=9.0.1+11-1
# Sat, 04 Nov 2017 01:31:39 GMT
RUN set -ex; 		if [ ! -d /usr/share/man/man1 ]; then 		mkdir -p /usr/share/man/man1; 	fi; 		apt-get update; 	apt-get install -y 		openjdk-9-jdk-headless="$JAVA_DEBIAN_VERSION" 	; 	rm -rf /var/lib/apt/lists/*; 		[ "$(readlink -f "$JAVA_HOME")" = "$(docker-java-home)" ]; 		update-alternatives --get-selections | awk -v home="$(readlink -f "$JAVA_HOME")" 'index($3, home) == 1 { $2 = "manual"; print | "update-alternatives --set-selections" }'; 	update-alternatives --query java | grep -q 'Status: manual'
# Sat, 04 Nov 2017 01:31:40 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:d96a59f9a30fc164a930c5f4118584e683bec40d1797f9d9bca30f65f3a647af`  
		Last Modified: Mon, 09 Oct 2017 21:51:14 GMT  
		Size: 21.6 MB (21639073 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c164bdc72bb7e7c356d01b6f09f139b666b9b352a4ddc54537fdaa48e8a0ad6`  
		Last Modified: Mon, 09 Oct 2017 23:27:15 GMT  
		Size: 436.4 KB (436444 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b40759634bf5c1bbde4c10d3cb802e1d71d31216cf2c389d566820272f1239ca`  
		Last Modified: Mon, 09 Oct 2017 23:27:15 GMT  
		Size: 247.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aaabb110ae529eef899672bd02ae789a08f5b8093187fded0073a6352a26493d`  
		Last Modified: Mon, 09 Oct 2017 23:27:15 GMT  
		Size: 131.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78602e9bfe5a6941bbd046ffc9d8ad27e67187f2eafe085b107df5349896e28c`  
		Last Modified: Sat, 04 Nov 2017 01:38:48 GMT  
		Size: 136.8 MB (136802715 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `openjdk:9-jdk-slim` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:06fff3184b5d9dbbaea16729bd680e926c054d0db762ad3a4a18cbd83dcb113c
```

-	Docker Version: 17.06.2-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **162.2 MB (162237847 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1e11c5474a82ef5ddc4740336a23dd1705ac58480965b3da828e376e092cca37`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 09 Oct 2017 21:45:50 GMT
ADD file:7734ca257bd7327a8da07cdcc881d2054c6cf50201f5bb0aeda8637c7e40cc06 in / 
# Mon, 09 Oct 2017 21:45:51 GMT
CMD ["bash"]
# Tue, 10 Oct 2017 01:49:51 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 	&& rm -rf /var/lib/apt/lists/*
# Tue, 10 Oct 2017 01:49:51 GMT
ENV LANG=C.UTF-8
# Tue, 10 Oct 2017 01:49:53 GMT
RUN { 		echo '#!/bin/sh'; 		echo 'set -e'; 		echo; 		echo 'dirname "$(dirname "$(readlink -f "$(which javac || which java)")")"'; 	} > /usr/local/bin/docker-java-home 	&& chmod +x /usr/local/bin/docker-java-home
# Tue, 10 Oct 2017 01:49:55 GMT
RUN ln -svT "/usr/lib/jvm/java-9-openjdk-$(dpkg --print-architecture)" /docker-java-home
# Tue, 10 Oct 2017 01:49:55 GMT
ENV JAVA_HOME=/docker-java-home
# Sat, 04 Nov 2017 12:49:20 GMT
ENV JAVA_VERSION=9.0.1+11
# Sat, 04 Nov 2017 12:49:21 GMT
ENV JAVA_DEBIAN_VERSION=9.0.1+11-1
# Sat, 04 Nov 2017 12:51:03 GMT
RUN set -ex; 		if [ ! -d /usr/share/man/man1 ]; then 		mkdir -p /usr/share/man/man1; 	fi; 		apt-get update; 	apt-get install -y 		openjdk-9-jdk-headless="$JAVA_DEBIAN_VERSION" 	; 	rm -rf /var/lib/apt/lists/*; 		[ "$(readlink -f "$JAVA_HOME")" = "$(docker-java-home)" ]; 		update-alternatives --get-selections | awk -v home="$(readlink -f "$JAVA_HOME")" 'index($3, home) == 1 { $2 = "manual"; print | "update-alternatives --set-selections" }'; 	update-alternatives --query java | grep -q 'Status: manual'
# Sat, 04 Nov 2017 12:51:04 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:9dc315cd342ed5fdb1c77afafbe657c1c29de0747c81d85f1f9ae06ad1d01fa4`  
		Last Modified: Mon, 09 Oct 2017 21:59:06 GMT  
		Size: 22.7 MB (22709128 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f96b1ccf72714886ea440013736b3705900f6f9751ec2664a26a9cb3042e3f0`  
		Last Modified: Tue, 10 Oct 2017 02:22:06 GMT  
		Size: 445.3 KB (445252 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09d7984bd0489b39fe260c46dcb9772e8656599426233067ad9af68b557e2d73`  
		Last Modified: Tue, 10 Oct 2017 02:22:06 GMT  
		Size: 246.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3682b3ee64dc20e447d8a52e66fd89da4f08cb2341fc1836b460609fc12eb0d`  
		Last Modified: Tue, 10 Oct 2017 02:22:06 GMT  
		Size: 131.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7652d1166158dd84f003cd12bfaf268458a9e4fb522f4999db3a30446c342af8`  
		Last Modified: Sat, 04 Nov 2017 13:20:13 GMT  
		Size: 139.1 MB (139083090 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `openjdk:9-jdk-slim` - linux; 386

```console
$ docker pull openjdk@sha256:33ead71044d44e8ec97daa32f7afb1195764badda81334c5911ad509219347dd
```

-	Docker Version: 17.06.2-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **185.7 MB (185707562 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:89aacf2eb31e6843416be768153dae9c7866d4e583ff9734b1580515b7823fda`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 09 Oct 2017 21:44:42 GMT
ADD file:19c55eeae4bfb6e75c713222705ba8d4849604df30a58a50860ac7bd205dfda4 in / 
# Mon, 09 Oct 2017 21:44:42 GMT
CMD ["bash"]
# Tue, 10 Oct 2017 01:28:05 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 	&& rm -rf /var/lib/apt/lists/*
# Tue, 10 Oct 2017 01:28:08 GMT
ENV LANG=C.UTF-8
# Tue, 10 Oct 2017 01:28:09 GMT
RUN { 		echo '#!/bin/sh'; 		echo 'set -e'; 		echo; 		echo 'dirname "$(dirname "$(readlink -f "$(which javac || which java)")")"'; 	} > /usr/local/bin/docker-java-home 	&& chmod +x /usr/local/bin/docker-java-home
# Tue, 10 Oct 2017 01:28:10 GMT
RUN ln -svT "/usr/lib/jvm/java-9-openjdk-$(dpkg --print-architecture)" /docker-java-home
# Tue, 10 Oct 2017 01:28:10 GMT
ENV JAVA_HOME=/docker-java-home
# Sat, 04 Nov 2017 10:19:28 GMT
ENV JAVA_VERSION=9.0.1+11
# Sat, 04 Nov 2017 10:19:28 GMT
ENV JAVA_DEBIAN_VERSION=9.0.1+11-1
# Sat, 04 Nov 2017 10:20:13 GMT
RUN set -ex; 		if [ ! -d /usr/share/man/man1 ]; then 		mkdir -p /usr/share/man/man1; 	fi; 		apt-get update; 	apt-get install -y 		openjdk-9-jdk-headless="$JAVA_DEBIAN_VERSION" 	; 	rm -rf /var/lib/apt/lists/*; 		[ "$(readlink -f "$JAVA_HOME")" = "$(docker-java-home)" ]; 		update-alternatives --get-selections | awk -v home="$(readlink -f "$JAVA_HOME")" 'index($3, home) == 1 { $2 = "manual"; print | "update-alternatives --set-selections" }'; 	update-alternatives --query java | grep -q 'Status: manual'
# Sat, 04 Nov 2017 10:20:13 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:8dbd94837ca8315beb351e1b4a4633d7694cecb75bd76e51339f9fc3d1362ea4`  
		Last Modified: Mon, 09 Oct 2017 21:51:23 GMT  
		Size: 25.7 MB (25658987 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4541ed9bcc08c4b1df4164753e37f6503b3dc167e45d1ee73bae5df2235d4bd5`  
		Last Modified: Tue, 10 Oct 2017 02:03:41 GMT  
		Size: 469.1 KB (469054 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7dc19ed4e40f01efc0a9b7e8728b3a714e8988d9988c655294a7cd0557e4fd4`  
		Last Modified: Tue, 10 Oct 2017 02:03:40 GMT  
		Size: 247.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6adbd212b15cf15807ba58d5148c502ce8708f3fb6e4b929f35ab3e2806ba9c`  
		Last Modified: Tue, 10 Oct 2017 02:03:40 GMT  
		Size: 131.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b64dfac1058e02c50bdf9a0fb7cacf820cdab30325c5b7254064be1e46677690`  
		Last Modified: Sat, 04 Nov 2017 10:52:22 GMT  
		Size: 159.6 MB (159579143 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `openjdk:9-jdk-slim` - linux; ppc64le

```console
$ docker pull openjdk@sha256:aaec76ff1caf8b2b8d08b68269fce06f4f5ccad49b96bf66c72d19d3eb1d8d21
```

-	Docker Version: 17.06.2-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **167.3 MB (167277043 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c7b14ec9e9b9c278c4f5c131197a6fad53e7bf3df3b5f956873a3d982febc594`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 09 Oct 2017 21:44:35 GMT
ADD file:975af260e7927569ddcee28239226e9deaf2ba539f038b467169340d69bc7072 in / 
# Mon, 09 Oct 2017 21:44:37 GMT
CMD ["bash"]
# Tue, 10 Oct 2017 04:37:45 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 	&& rm -rf /var/lib/apt/lists/*
# Tue, 10 Oct 2017 04:37:48 GMT
ENV LANG=C.UTF-8
# Tue, 10 Oct 2017 04:37:54 GMT
RUN { 		echo '#!/bin/sh'; 		echo 'set -e'; 		echo; 		echo 'dirname "$(dirname "$(readlink -f "$(which javac || which java)")")"'; 	} > /usr/local/bin/docker-java-home 	&& chmod +x /usr/local/bin/docker-java-home
# Tue, 10 Oct 2017 04:38:01 GMT
RUN ln -svT "/usr/lib/jvm/java-9-openjdk-$(dpkg --print-architecture)" /docker-java-home
# Tue, 10 Oct 2017 04:38:05 GMT
ENV JAVA_HOME=/docker-java-home
# Sat, 04 Nov 2017 11:11:26 GMT
ENV JAVA_VERSION=9.0.1+11
# Sat, 04 Nov 2017 11:11:27 GMT
ENV JAVA_DEBIAN_VERSION=9.0.1+11-1
# Sat, 04 Nov 2017 11:13:19 GMT
RUN set -ex; 		if [ ! -d /usr/share/man/man1 ]; then 		mkdir -p /usr/share/man/man1; 	fi; 		apt-get update; 	apt-get install -y 		openjdk-9-jdk-headless="$JAVA_DEBIAN_VERSION" 	; 	rm -rf /var/lib/apt/lists/*; 		[ "$(readlink -f "$JAVA_HOME")" = "$(docker-java-home)" ]; 		update-alternatives --get-selections | awk -v home="$(readlink -f "$JAVA_HOME")" 'index($3, home) == 1 { $2 = "manual"; print | "update-alternatives --set-selections" }'; 	update-alternatives --query java | grep -q 'Status: manual'
# Sat, 04 Nov 2017 11:13:21 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:58316d9a92e4d6154c1ca7f3d20c3fe96a2931387507b6226b9bcb094ebf13a1`  
		Last Modified: Mon, 09 Oct 2017 21:51:05 GMT  
		Size: 25.9 MB (25935856 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2cb131ef3a79b457ff98e269a64ece4b6e5a2b846dfeffe8d816ad700c89eb1`  
		Last Modified: Tue, 10 Oct 2017 05:22:45 GMT  
		Size: 455.2 KB (455170 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4af6ed7bad84f73f72309cd6fd34c5f02d380a962d70be083f47f50011e29f8b`  
		Last Modified: Tue, 10 Oct 2017 05:22:46 GMT  
		Size: 247.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c81bf7c16727685616c16f67bbedf2377b69b2b65856f76e421844e15d28208`  
		Last Modified: Tue, 10 Oct 2017 05:22:45 GMT  
		Size: 133.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b540a6a05354c9463b32c1cab8c76aaa847b50008707cf96057fb5280a45bc04`  
		Last Modified: Sat, 04 Nov 2017 11:27:47 GMT  
		Size: 140.9 MB (140885637 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `openjdk:9-jdk-slim` - linux; s390x

```console
$ docker pull openjdk@sha256:6e0bbad7b2f14b3391b7dbfec49b7728659794d2fed46088ab4e6ccb22f30df3
```

-	Docker Version: 17.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **165.9 MB (165867284 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:61104e7d0fa88f00afb617f0855c7badf604dde1ba25f3697127343da55d8b75`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 09 Oct 2017 21:43:37 GMT
ADD file:b4deb6fb528f8c816ba7db3484f7590bf072a683b2d2bf4b616ac44850e10494 in / 
# Mon, 09 Oct 2017 21:43:38 GMT
CMD ["bash"]
# Mon, 09 Oct 2017 22:56:38 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 	&& rm -rf /var/lib/apt/lists/*
# Mon, 09 Oct 2017 22:56:38 GMT
ENV LANG=C.UTF-8
# Mon, 09 Oct 2017 22:56:38 GMT
RUN { 		echo '#!/bin/sh'; 		echo 'set -e'; 		echo; 		echo 'dirname "$(dirname "$(readlink -f "$(which javac || which java)")")"'; 	} > /usr/local/bin/docker-java-home 	&& chmod +x /usr/local/bin/docker-java-home
# Mon, 09 Oct 2017 22:56:41 GMT
RUN ln -svT "/usr/lib/jvm/java-9-openjdk-$(dpkg --print-architecture)" /docker-java-home
# Mon, 09 Oct 2017 22:56:44 GMT
ENV JAVA_HOME=/docker-java-home
# Sat, 04 Nov 2017 17:00:03 GMT
ENV JAVA_VERSION=9.0.1+11
# Sat, 04 Nov 2017 17:00:03 GMT
ENV JAVA_DEBIAN_VERSION=9.0.1+11-1
# Sat, 04 Nov 2017 17:00:46 GMT
RUN set -ex; 		if [ ! -d /usr/share/man/man1 ]; then 		mkdir -p /usr/share/man/man1; 	fi; 		apt-get update; 	apt-get install -y 		openjdk-9-jdk-headless="$JAVA_DEBIAN_VERSION" 	; 	rm -rf /var/lib/apt/lists/*; 		[ "$(readlink -f "$JAVA_HOME")" = "$(docker-java-home)" ]; 		update-alternatives --get-selections | awk -v home="$(readlink -f "$JAVA_HOME")" 'index($3, home) == 1 { $2 = "manual"; print | "update-alternatives --set-selections" }'; 	update-alternatives --query java | grep -q 'Status: manual'
# Sat, 04 Nov 2017 17:00:46 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:044c9ae4e8107afdcd4e6b93a76f7d598ae117778f3cf7dacd9d6087e3ac4f3b`  
		Last Modified: Mon, 09 Oct 2017 21:47:55 GMT  
		Size: 24.6 MB (24643207 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9070e5b963f9d96e62e6d5bd2a1e800f7745293b6bf97e423d883ad4cb6a280d`  
		Last Modified: Mon, 09 Oct 2017 23:04:14 GMT  
		Size: 471.4 KB (471352 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2624213d4686ead64a27d4dac297ad322ddab0cf41272465a4cd53620bcbd47b`  
		Last Modified: Mon, 09 Oct 2017 23:04:14 GMT  
		Size: 247.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3c076a1ba6889dcaf5124d6f37956b4265b3b023a96bbdd23780ad89cb3cf18`  
		Last Modified: Mon, 09 Oct 2017 23:04:15 GMT  
		Size: 132.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:baafe382c5aac70dc0e87d231167dbbd6971b26b1ac5361ddeeb3d18af6f276c`  
		Last Modified: Sat, 04 Nov 2017 17:06:27 GMT  
		Size: 140.8 MB (140752346 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
