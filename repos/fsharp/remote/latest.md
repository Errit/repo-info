## `fsharp:latest`

```console
$ docker pull fsharp@sha256:441b6f636383db772ba6267f0a78a0eef6aaaff8987411c04978f30c4ca6d69c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `fsharp:latest` - linux; amd64

```console
$ docker pull fsharp@sha256:6bddcbb2037682c3aafdb3e289e8980a548586cb31cf42d71e39f535b0ddff40
```

-	Docker Version: 17.06.2-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **176.0 MB (175975435 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:88de5e3e9e9187bb462d81be38fe94fe401cd080169d1f28ec67cf57eea9fe7b`
-	Default Command: `["fsharpi"]`

```dockerfile
# Sat, 04 Nov 2017 05:22:35 GMT
ADD file:187fe0df97a4c52984a518a454fb7ab3984ae7b541ede7ff84dd3c5da1ce1a59 in / 
# Sat, 04 Nov 2017 05:22:36 GMT
CMD ["bash"]
# Sat, 04 Nov 2017 13:11:51 GMT
LABEL maintainer=Dave Curylo <dave@curylo.org>, Steve Desmond <steve@stevedesmond.ca>
# Sat, 04 Nov 2017 13:11:51 GMT
ENV MONO_THREADS_PER_CPU=50
# Sat, 04 Nov 2017 13:28:21 GMT
RUN MONO_VERSION=5.2.0.224 &&     FSHARP_VERSION=4.1.28 &&     FSHARP_PREFIX=/usr &&     FSHARP_GACDIR=/usr/lib/mono/gac &&     FSHARP_BASENAME=fsharp-$FSHARP_VERSION &&     FSHARP_ARCHIVE=$FSHARP_VERSION.tar.gz &&     FSHARP_ARCHIVE_URL=https://github.com/fsharp/fsharp/archive/$FSHARP_VERSION.tar.gz &&     apt-key adv --keyserver hkp://p80.pool.sks-keyservers.net:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF &&     echo "deb http://download.mono-project.com/repo/debian jessie/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official.list &&     apt-get update -y &&     apt-get --no-install-recommends install -y autoconf libtool pkg-config make automake nuget mono-devel msbuild ca-certificates-mono &&     rm -rf /var/lib/apt/lists/* &&     mkdir -p /tmp/src &&     cd /tmp/src &&     printf "namespace a { class b { public static void Main(string[] args) { new System.Net.WebClient().DownloadFile(\"%s\", \"%s\");}}}" $FSHARP_ARCHIVE_URL $FSHARP_ARCHIVE > download-fsharp.cs &&     mcs download-fsharp.cs && mono download-fsharp.exe && rm download-fsharp.exe download-fsharp.cs &&     tar xf $FSHARP_ARCHIVE &&     cd $FSHARP_BASENAME &&     ./autogen.sh --prefix=$FSHARP_PREFIX --with-gacdir=$FSHARP_GACDIR &&     make &&     make install &&     cd ~ &&     rm -rf /tmp/src /tmp/NuGetScratch ~/.nuget ~/.config ~/.local &&     apt-get purge -y autoconf libtool make automake &&     apt-get clean
# Sat, 04 Nov 2017 13:28:37 GMT
WORKDIR /root
# Sat, 04 Nov 2017 13:28:37 GMT
CMD ["fsharpi"]
```

-	Layers:
	-	`sha256:d13d02fa248db2b423d6dbc8ec435675d23122f3939b5278b2156b75258e2259`  
		Last Modified: Mon, 09 Oct 2017 21:37:31 GMT  
		Size: 30.1 MB (30113318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7bd449a229a84c2c243c38a429f5979f1da1280727dece48646755b2b34bb198`  
		Last Modified: Sat, 04 Nov 2017 14:04:49 GMT  
		Size: 145.9 MB (145862117 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
