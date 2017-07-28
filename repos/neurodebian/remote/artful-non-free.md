## `neurodebian:artful-non-free`

```console
$ docker pull neurodebian@sha256:940478e9e01184ed6480819e5b233d25099595d2e372dd789ec97ebb41deb060
```

-	Platforms:
	-	linux; amd64

### `neurodebian:artful-non-free` - linux; amd64

-	Docker Version: 17.03.2-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **40.6 MB (40596587 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6488565859fadb46752772211f54dfdda0a2d03c7fe6b6a7a029dc5d25d5c457`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 20 Jul 2017 17:13:41 GMT
ADD file:ccb8cc1116dd151142af17223e206ab67d45ed86bdb1f3daf6f202f78aa1ceda in / 
# Thu, 20 Jul 2017 17:13:42 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 20 Jul 2017 17:13:43 GMT
RUN rm -rf /var/lib/apt/lists/*
# Thu, 20 Jul 2017 17:13:45 GMT
RUN sed -i 's/^#\s*\(deb.*universe\)$/\1/g' /etc/apt/sources.list
# Thu, 20 Jul 2017 17:13:46 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 20 Jul 2017 17:13:46 GMT
CMD ["/bin/bash"]
# Thu, 20 Jul 2017 20:11:55 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg2 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Thu, 20 Jul 2017 20:11:59 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --keyserver ha.pool.sks-keyservers.net --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Thu, 20 Jul 2017 20:12:00 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian artful main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel artful main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Thu, 27 Jul 2017 19:44:07 GMT
RUN sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list; grep -q 'deb .* multiverse$' /etc/apt/sources.list || sed -i -e 's,universe *$,universe multiverse,g' /etc/apt/sources.list
```

-	Layers:
	-	`sha256:619e287e5b4b0df2b90cea3d6ad56f438e08e48d2a585cd8df806328e8e4c95e`  
		Last Modified: Thu, 20 Jul 2017 17:16:45 GMT  
		Size: 38.9 MB (38895747 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:697e8d291b3785acaaebbbc0dca4acf0cf1ef1b4e83733e8b4f894f2d98bef0b`  
		Last Modified: Thu, 20 Jul 2017 17:16:39 GMT  
		Size: 815.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ab1564e1ab0cdfedb15e86f686334eaca6e3a15a7f70d8944cee00862c251bf`  
		Last Modified: Thu, 20 Jul 2017 17:16:40 GMT  
		Size: 391.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a186ea1e4d3838f7f614b0083f1694828a7ce2be4a890b159402247a9a3a0aa`  
		Last Modified: Thu, 20 Jul 2017 17:16:39 GMT  
		Size: 850.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7dd9f9ae752925cb019e61080ffd902c8bfcc23af9ee3b61d82abee91608ab00`  
		Last Modified: Thu, 20 Jul 2017 17:16:39 GMT  
		Size: 163.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54d5cf99637a77d0e4bb92f237e2cc4ee5bbe782c1adac780c858db35299cf32`  
		Last Modified: Thu, 20 Jul 2017 20:13:17 GMT  
		Size: 1.7 MB (1694999 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3f8ddc8e4b3c00d1d40d23188719356b0206107ffc0f3f73e233b243b9f0a12`  
		Last Modified: Thu, 20 Jul 2017 20:13:17 GMT  
		Size: 3.1 KB (3136 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92eb7e793eafef6e97d2c465ed5909c27a31ba2a8ec20939356f7515f8f3045e`  
		Last Modified: Thu, 20 Jul 2017 20:13:17 GMT  
		Size: 237.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:33ea5d3f4e52aa00fffd8c99a6a85ea58be1f4b3ead2d58ffd2da1b30bbe96cd`  
		Last Modified: Thu, 27 Jul 2017 19:57:47 GMT  
		Size: 249.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip