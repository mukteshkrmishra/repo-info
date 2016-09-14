## `orientdb:latest`

```console
$ docker pull orientdb@sha256:8a18d5d3f7a28148aed6a18c5924dddd7fb0145f9079b44a26dac9ce8945f943
```

-	Platforms:
	-	linux; amd64

### `orientdb:latest` - linux; amd64

-	Docker Version: 1.12.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **86.8 MB (86844656 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:247443cd19a80260de087bea845fa239b019811c9a8b6c1fb80115be9f18b79c`
-	Default Command: `["server.sh"]`

```dockerfile
# Mon, 29 Aug 2016 23:49:14 GMT
ADD file:852e9d0cb9d906535af512a89339fc70b2873a0f94defbcbe41cd44942dd6ac8 in / 
# Tue, 30 Aug 2016 19:53:16 GMT
ENV LANG=C.UTF-8
# Tue, 30 Aug 2016 19:53:17 GMT
RUN { 		echo '#!/bin/sh'; 		echo 'set -e'; 		echo; 		echo 'dirname "$(dirname "$(readlink -f "$(which javac || which java)")")"'; 	} > /usr/local/bin/docker-java-home 	&& chmod +x /usr/local/bin/docker-java-home
# Tue, 30 Aug 2016 19:55:33 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-1.8-openjdk
# Tue, 30 Aug 2016 19:55:33 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/java-1.8-openjdk/jre/bin:/usr/lib/jvm/java-1.8-openjdk/bin
# Tue, 30 Aug 2016 19:55:34 GMT
ENV JAVA_VERSION=8u92
# Tue, 30 Aug 2016 19:55:34 GMT
ENV JAVA_ALPINE_VERSION=8.92.14-r1
# Tue, 30 Aug 2016 19:55:39 GMT
RUN set -x 	&& apk add --no-cache 		openjdk8="$JAVA_ALPINE_VERSION" 	&& [ "$JAVA_HOME" = "$(docker-java-home)" ]
# Tue, 30 Aug 2016 20:25:04 GMT
MAINTAINER OrientDB LTD (info@orientdb.com)
# Tue, 30 Aug 2016 20:25:11 GMT
ARG ORIENTDB_DOWNLOAD_SERVER
# Thu, 08 Sep 2016 17:33:54 GMT
ENV ORIENTDB_VERSION=2.2.9
# Thu, 08 Sep 2016 17:33:54 GMT
ENV ORIENTDB_DOWNLOAD_MD5=a37dca4c9f6304e76663fbc2b71d1d3a
# Thu, 08 Sep 2016 17:33:54 GMT
ENV ORIENTDB_DOWNLOAD_SHA1=17146d6b6340a39db28ca82ae821057646c154fc
# Thu, 08 Sep 2016 17:33:55 GMT
ENV ORIENTDB_DOWNLOAD_URL=http://central.maven.org/maven2/com/orientechnologies/orientdb-community/2.2.9/orientdb-community-2.2.9.tar.gz
# Thu, 08 Sep 2016 17:33:56 GMT
RUN apk add --update tar     && rm -rf /var/cache/apk/*
# Thu, 08 Sep 2016 17:33:59 GMT
RUN mkdir /orientdb &&   wget  $ORIENTDB_DOWNLOAD_URL   && echo "$ORIENTDB_DOWNLOAD_MD5 *orientdb-community-$ORIENTDB_VERSION.tar.gz" | md5sum -c -   && echo "$ORIENTDB_DOWNLOAD_SHA1 *orientdb-community-$ORIENTDB_VERSION.tar.gz" | sha1sum -c -   && tar -xvzf orientdb-community-$ORIENTDB_VERSION.tar.gz -C /orientdb --strip-components=1   && rm orientdb-community-$ORIENTDB_VERSION.tar.gz   && rm -rf /orientdb/databases/*
# Thu, 08 Sep 2016 17:33:59 GMT
ENV PATH=/orientdb/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/java-1.8-openjdk/jre/bin:/usr/lib/jvm/java-1.8-openjdk/bin
# Thu, 08 Sep 2016 17:34:00 GMT
VOLUME [/orientdb/backup /orientdb/databases /orientdb/config]
# Thu, 08 Sep 2016 17:34:00 GMT
WORKDIR /orientdb
# Thu, 08 Sep 2016 17:34:01 GMT
EXPOSE 2424/tcp
# Thu, 08 Sep 2016 17:34:01 GMT
EXPOSE 2480/tcp
# Thu, 08 Sep 2016 17:34:01 GMT
CMD ["server.sh"]
```

-	Layers:
	-	`sha256:e110a4a1794126ef308a49f2d65785af2f25538f06700721aad8283b81fdfa58`  
		Last Modified: Thu, 23 Jun 2016 19:56:16 GMT  
		Size: 2.3 MB (2310286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a696cba1f6e865421664a7bf9bf585bcfaa924d56b7d2a112a799e00a7433791`  
		Last Modified: Tue, 30 Aug 2016 21:11:27 GMT  
		Size: 232.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0f0d61cd0d229546b1e33b0c92036ad3f35b42dd2c9a945aeaf67f84684ce26`  
		Last Modified: Tue, 30 Aug 2016 21:56:07 GMT  
		Size: 49.3 MB (49325330 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b67e57752b3062014629539db0d1fdcc36fa03ba9ae0af85049dfb3edd1e139`  
		Last Modified: Thu, 08 Sep 2016 17:34:31 GMT  
		Size: 261.8 KB (261817 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d43629e2088a6334fd0cbdb5c65e2bc00f5dfb5857ad7594b3421e1a28ce8fd`  
		Last Modified: Thu, 08 Sep 2016 17:34:36 GMT  
		Size: 34.9 MB (34946991 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip