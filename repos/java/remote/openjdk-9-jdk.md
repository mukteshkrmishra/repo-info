## `java:openjdk-9-jdk`

```console
$ docker pull java@sha256:dadb5ed28780e2871f165bf217feda44bab10dcced4263b7fba95674b6ddadf4
```

-	Platforms:
	-	linux; amd64

### `java:openjdk-9-jdk` - linux; amd64

-	Docker Version: 1.12.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **245.1 MB (245118659 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d2c71df7073650ad622ed16bb737574595ce9bf63b36cfb44d0156dae69875ae`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 23 Sep 2016 18:09:05 GMT
ADD file:38fc3f9aecc8de28ee67c48e4f26a9dd74b238023b7f92c19da2f642b9d0fc14 in / 
# Fri, 23 Sep 2016 18:09:06 GMT
CMD ["/bin/bash"]
# Fri, 23 Sep 2016 18:27:12 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		wget 	&& rm -rf /var/lib/apt/lists/*
# Fri, 23 Sep 2016 18:27:51 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Fri, 23 Sep 2016 19:39:17 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 	&& rm -rf /var/lib/apt/lists/*
# Fri, 23 Sep 2016 19:39:18 GMT
RUN echo 'deb http://httpredir.debian.org/debian experimental main' > /etc/apt/sources.list.d/experimental.list
# Fri, 23 Sep 2016 19:39:18 GMT
ENV LANG=C.UTF-8
# Fri, 23 Sep 2016 19:39:19 GMT
RUN { 		echo '#!/bin/sh'; 		echo 'set -e'; 		echo; 		echo 'dirname "$(dirname "$(readlink -f "$(which javac || which java)")")"'; 	} > /usr/local/bin/docker-java-home 	&& chmod +x /usr/local/bin/docker-java-home
# Fri, 23 Sep 2016 19:39:19 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-9-openjdk-amd64
# Fri, 23 Sep 2016 19:39:19 GMT
ENV JAVA_VERSION=9~b136
# Fri, 23 Sep 2016 19:39:20 GMT
ENV JAVA_DEBIAN_VERSION=9~b136-1
# Fri, 23 Sep 2016 19:39:56 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y 		openjdk-9-jdk-headless="$JAVA_DEBIAN_VERSION" 	&& rm -rf /var/lib/apt/lists/* 	&& [ "$JAVA_HOME" = "$(docker-java-home)" ]
```

-	Layers:
	-	`sha256:8d7c8b969090899eedb896dfcdfc11e08596be2a94b1ae77609086ede354ab53`  
		Last Modified: Fri, 23 Sep 2016 18:11:54 GMT  
		Size: 43.1 MB (43149672 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b5cf27ef20a0d684a2f113fab4b3cf58cdb4b5e3ec312e688e979add4df4d9cb`  
		Last Modified: Fri, 23 Sep 2016 18:27:26 GMT  
		Size: 20.6 MB (20558939 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d346a7dd355fc6b042ab875c346181e3a59830f2c0a2961b7512dfc171eb8950`  
		Last Modified: Fri, 23 Sep 2016 18:28:16 GMT  
		Size: 52.3 MB (52334181 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a61c0ce2aaf48ece0d079535a6ae3a75d760f88be32e826f39042b07a2fd4d95`  
		Last Modified: Fri, 23 Sep 2016 19:40:05 GMT  
		Size: 592.5 KB (592473 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d454d9b918097dbfabf38bbb570310a8e69aae04066af9025a14f1970956918`  
		Last Modified: Fri, 23 Sep 2016 19:40:03 GMT  
		Size: 216.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6698e2f319714131e15680242720372f8ebc7da860484cc00e21f2bb0d9e3ad`  
		Last Modified: Fri, 23 Sep 2016 19:40:03 GMT  
		Size: 242.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:688ee1a7ff8dfa0cd12e4cc0458513f2fc461c0f92135f5a6162fca1a6b7dd31`  
		Last Modified: Fri, 23 Sep 2016 19:40:24 GMT  
		Size: 128.5 MB (128482936 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
