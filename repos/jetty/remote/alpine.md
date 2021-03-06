## `jetty:alpine`

```console
$ docker pull jetty@sha256:c69bb1113f827ad2289beced710e03d610b562133c457c3ba5814619d5fae2cf
```

-	Platforms:
	-	linux; amd64

### `jetty:alpine` - linux; amd64

-	Docker Version: 1.12.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.9 MB (49907475 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a497aa03f8529658fc2d1b785eb60ec1cde2d9e010e725ac4e36c1e80966da40`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["java","-jar","\/usr\/local\/jetty\/start.jar"]`

```dockerfile
# Fri, 23 Sep 2016 16:29:57 GMT
ADD file:d6ee3ba7a4d59b161917082cc7242c660c61bb3f3cc1549c7e2dfff2b0de7104 in / 
# Fri, 23 Sep 2016 17:02:28 GMT
ENV LANG=C.UTF-8
# Fri, 23 Sep 2016 17:02:29 GMT
RUN { 		echo '#!/bin/sh'; 		echo 'set -e'; 		echo; 		echo 'dirname "$(dirname "$(readlink -f "$(which javac || which java)")")"'; 	} > /usr/local/bin/docker-java-home 	&& chmod +x /usr/local/bin/docker-java-home
# Fri, 23 Sep 2016 17:07:01 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-1.8-openjdk/jre
# Fri, 23 Sep 2016 17:07:01 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/java-1.8-openjdk/jre/bin:/usr/lib/jvm/java-1.8-openjdk/bin
# Fri, 23 Sep 2016 17:07:01 GMT
ENV JAVA_VERSION=8u92
# Fri, 23 Sep 2016 17:07:02 GMT
ENV JAVA_ALPINE_VERSION=8.92.14-r1
# Fri, 23 Sep 2016 17:07:05 GMT
RUN set -x 	&& apk add --no-cache 		openjdk8-jre="$JAVA_ALPINE_VERSION" 	&& [ "$JAVA_HOME" = "$(docker-java-home)" ]
# Fri, 23 Sep 2016 18:52:35 GMT
RUN addgroup -S jetty && adduser -D -S -H -G jetty jetty && rm -rf /etc/group- /etc/passwd- /etc/shadow-
# Fri, 23 Sep 2016 18:52:35 GMT
ENV JETTY_HOME=/usr/local/jetty
# Fri, 23 Sep 2016 18:52:35 GMT
ENV PATH=/usr/local/jetty/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/java-1.8-openjdk/jre/bin:/usr/lib/jvm/java-1.8-openjdk/bin
# Fri, 23 Sep 2016 18:52:36 GMT
RUN mkdir -p "$JETTY_HOME"
# Fri, 23 Sep 2016 18:52:37 GMT
WORKDIR /usr/local/jetty
# Fri, 23 Sep 2016 18:52:37 GMT
ENV JETTY_BASE=/var/lib/jetty
# Fri, 23 Sep 2016 18:52:38 GMT
RUN mkdir -p "$JETTY_BASE"
# Fri, 23 Sep 2016 18:52:39 GMT
ENV JETTY_VERSION=9.3.11.v20160721
# Fri, 23 Sep 2016 18:52:39 GMT
ENV JETTY_TGZ_URL=https://repo1.maven.org/maven2/org/eclipse/jetty/jetty-distribution/9.3.11.v20160721/jetty-distribution-9.3.11.v20160721.tar.gz
# Fri, 23 Sep 2016 18:52:39 GMT
ENV JETTY_GPG_KEYS=B59B67FD7904984367F931800818D9D68FB67BAC 	5DE533CB43DAF8BC3E372283E7AE839CD7C58886
# Fri, 23 Sep 2016 18:52:50 GMT
RUN set -xe 	&& apk add --no-cache --virtual .build-deps gnupg coreutils curl 	&& curl -SL "$JETTY_TGZ_URL" -o jetty.tar.gz 	&& curl -SL "$JETTY_TGZ_URL.asc" -o jetty.tar.gz.asc 	&& export GNUPGHOME="$(mktemp -d)" 	&& for key in $JETTY_GPG_KEYS; do 		gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; done 	&& gpg --batch --verify jetty.tar.gz.asc jetty.tar.gz 	&& rm -r "$GNUPGHOME" 	&& tar -xvzf jetty.tar.gz 	&& mv jetty-distribution-$JETTY_VERSION/* ./ 	&& sed -i '/jetty-logging/d' etc/jetty.conf 	&& rm -fr demo-base javadoc 	&& rm jetty.tar.gz* 	&& rm -fr jetty-distribution-$JETTY_VERSION/ 	&& cd $JETTY_BASE 	&& modules="$(grep -- ^--module= "$JETTY_HOME/start.ini" | cut -d= -f2 | paste -d, -s)" 	&& java -jar "$JETTY_HOME/start.jar" --add-to-startd="$modules,setuid" 	&& apk del .build-deps 	&& rm -fr .build-deps 	&& rm -rf /tmp/hsperfdata_root
# Fri, 23 Sep 2016 18:52:50 GMT
WORKDIR /var/lib/jetty
# Fri, 23 Sep 2016 18:52:51 GMT
ENV TMPDIR=/tmp/jetty
# Fri, 23 Sep 2016 18:52:52 GMT
RUN set -xe 	&& mkdir -p "$TMPDIR" 	&& chown -R jetty:jetty "$TMPDIR" "$JETTY_BASE"
# Fri, 23 Sep 2016 18:52:52 GMT
COPY file:4f7da2906a90932cfb90db54a45ee08f86b17253747db62085f7512c9efd46ad in / 
# Fri, 23 Sep 2016 18:52:53 GMT
EXPOSE 8080/tcp
# Fri, 23 Sep 2016 18:52:53 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 23 Sep 2016 18:52:53 GMT
CMD ["java" "-jar" "/usr/local/jetty/start.jar"]
```

-	Layers:
	-	`sha256:c0cb142e43453ebb1f82b905aa472e6e66017efd43872135bc5372e4fac04031`  
		Last Modified: Fri, 23 Sep 2016 16:30:54 GMT  
		Size: 2.3 MB (2312930 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf00e3870fb3e40e4a8e049bc0cd0d95ccd634da7b4b9980004b819f064fa174`  
		Last Modified: Fri, 23 Sep 2016 17:02:49 GMT  
		Size: 231.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69001e8f079b82a7067ea481b58cb7076d7e3154a5e2da4b8eb4fc9670ebab2d`  
		Last Modified: Fri, 23 Sep 2016 17:07:21 GMT  
		Size: 39.6 MB (39647465 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e01910cc8a39ef3ca5bba16c7414c6533327fc8feb0c42b6cd1a59ee94bd781`  
		Last Modified: Fri, 23 Sep 2016 18:53:06 GMT  
		Size: 1.1 KB (1112 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b89216811b2bc12a5ebd83afed18122beb8d259fb6d9300e9c4d35d9b45af5e`  
		Last Modified: Fri, 23 Sep 2016 18:53:02 GMT  
		Size: 131.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d3682f556cfe6678e4f38e6652d6fe1deceea0888acbfd171d16d6663deea38a`  
		Last Modified: Fri, 23 Sep 2016 18:53:02 GMT  
		Size: 130.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e055bd5708e35457cb92c4b08de89f8ca5d9f44bdf6039992d8f526f59a1bfe`  
		Last Modified: Fri, 23 Sep 2016 18:53:05 GMT  
		Size: 7.9 MB (7943074 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0893345a8ef86d271493221225c3dfdbe096a2e3730d395a323c818a7da6fa90`  
		Last Modified: Fri, 23 Sep 2016 18:53:02 GMT  
		Size: 1.8 KB (1832 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:791e06bef9afb4d803d3c8e51fb8f41690e7d235b7e6c34e31427da5c2c8e01a`  
		Last Modified: Fri, 23 Sep 2016 18:53:02 GMT  
		Size: 570.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
