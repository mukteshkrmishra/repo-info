## `memcached:latest`

```console
$ docker pull memcached@sha256:7d78eaec16ea2fcc08550bd6cb3291ecc2e4c06882415c04baefc837c53bc58a
```

-	Platforms:
	-	linux; amd64

### `memcached:latest` - linux; amd64

-	Docker Version: 1.12.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.2 MB (52227197 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:880449bd1a8630a9ca55bc3d36ffcd042004fad423a9c3734a97e08254a63652`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Fri, 23 Sep 2016 18:08:50 GMT
ADD file:c6c23585ab140b0b320d4e99bc1b0eb544c9e96c24d90fec5e069a6d57d335ca in / 
# Fri, 23 Sep 2016 18:08:51 GMT
CMD ["/bin/bash"]
# Fri, 23 Sep 2016 20:03:22 GMT
RUN groupadd -r memcache && useradd -r -g memcache memcache
# Fri, 23 Sep 2016 20:03:30 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		libevent-2.0-5 	&& rm -rf /var/lib/apt/lists/*
# Fri, 23 Sep 2016 20:03:30 GMT
ENV MEMCACHED_VERSION=1.4.31
# Fri, 23 Sep 2016 20:03:30 GMT
ENV MEMCACHED_SHA1=3ea34f5bc5c5aacb76cfc07f4ee5847f33526cb6
# Fri, 23 Sep 2016 20:03:57 GMT
RUN buildDeps=' 		gcc 		libc6-dev 		libevent-dev 		make 		perl 		wget 	' 	&& set -x 	&& apt-get update && apt-get install -y $buildDeps --no-install-recommends 	&& rm -rf /var/lib/apt/lists/* 	&& wget -O memcached.tar.gz "http://memcached.org/files/memcached-$MEMCACHED_VERSION.tar.gz" 	&& echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c - 	&& mkdir -p /usr/src/memcached 	&& tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1 	&& rm memcached.tar.gz 	&& cd /usr/src/memcached 	&& ./configure 	&& make -j$(nproc) 	&& make install 	&& cd / && rm -rf /usr/src/memcached 	&& apt-get purge -y --auto-remove $buildDeps
# Fri, 23 Sep 2016 20:03:57 GMT
COPY file:621e178b267679ef7140edd23c3ad9e717ed767ed55322a4e198798311bc1d36 in /usr/local/bin/ 
# Fri, 23 Sep 2016 20:03:58 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Fri, 23 Sep 2016 20:03:59 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 23 Sep 2016 20:03:59 GMT
USER [memcache]
# Fri, 23 Sep 2016 20:03:59 GMT
EXPOSE 11211/tcp
# Fri, 23 Sep 2016 20:04:00 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:6a5a5368e0c2d3e5909184fa28ddfd56072e7ff3ee9a945876f7eee5896ef5bb`  
		Last Modified: Fri, 23 Sep 2016 18:10:19 GMT  
		Size: 51.4 MB (51354364 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5454a3272872da62e6bde09965cd50c416577f47324958c699a36c733b84ea8e`  
		Last Modified: Fri, 23 Sep 2016 20:04:08 GMT  
		Size: 2.0 KB (2039 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25a4deb16fc7c45fd59208bfb892b4c642398690fd82fa3719358f60f5b6b13b`  
		Last Modified: Fri, 23 Sep 2016 20:04:08 GMT  
		Size: 237.6 KB (237564 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c72fe4d2ac4b73a1c6969cbc455453a915eabedb7968a3db99715123de25493`  
		Last Modified: Fri, 23 Sep 2016 20:04:07 GMT  
		Size: 632.8 KB (632824 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ff82fad05cfa56f775f4b1cddc943caa33ce71a592a116ddce9b6b4f44af5c4`  
		Last Modified: Fri, 23 Sep 2016 20:04:07 GMT  
		Size: 286.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4683cc57b57b3b82b9836e9ce6d11ade50b8cfa62e3981c3ce61c7f9f8e6587`  
		Last Modified: Fri, 23 Sep 2016 20:04:07 GMT  
		Size: 120.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
