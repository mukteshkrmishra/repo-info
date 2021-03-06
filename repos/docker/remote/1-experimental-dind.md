## `docker:1-experimental-dind`

```console
$ docker pull docker@sha256:db17dd4f5b6f44f2cfba01ef0e1d591b2af1bb74c9fc0d3a6bc8ecffb6069218
```

-	Platforms:
	-	linux; amd64

### `docker:1-experimental-dind` - linux; amd64

-	Docker Version: 1.12.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.1 MB (34143939 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0d66c14b3aab7f7dd00d93fbe52da954550bcb732caadcf90a178293d576c5a3`
-	Entrypoint: `["dockerd-entrypoint.sh"]`
-	Default Command: `[]`

```dockerfile
# Fri, 23 Sep 2016 16:29:57 GMT
ADD file:d6ee3ba7a4d59b161917082cc7242c660c61bb3f3cc1549c7e2dfff2b0de7104 in / 
# Fri, 23 Sep 2016 16:36:54 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl
# Fri, 23 Sep 2016 16:38:38 GMT
ENV DOCKER_BUCKET=experimental.docker.com
# Fri, 23 Sep 2016 16:38:38 GMT
ENV DOCKER_VERSION=1.12.1
# Fri, 23 Sep 2016 16:38:38 GMT
ENV DOCKER_SHA256=f92fe0630dd1f20d9678cd7e4043018566e3737001f53171274a4a6ed6baaa08
# Fri, 23 Sep 2016 16:38:44 GMT
RUN set -x 	&& curl -fSL "https://${DOCKER_BUCKET}/builds/Linux/x86_64/docker-${DOCKER_VERSION}.tgz" -o docker.tgz 	&& echo "${DOCKER_SHA256} *docker.tgz" | sha256sum -c - 	&& tar -xzvf docker.tgz 	&& mv docker/* /usr/local/bin/ 	&& rmdir docker 	&& rm docker.tgz 	&& docker -v
# Fri, 23 Sep 2016 16:38:45 GMT
COPY file:50006c902e7677711aeffe4ab7b7042d649618b96dec760f322a8566dd83ab25 in /usr/local/bin/ 
# Fri, 23 Sep 2016 16:38:45 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 23 Sep 2016 16:38:45 GMT
CMD ["sh"]
# Fri, 23 Sep 2016 16:39:43 GMT
RUN apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		iptables 		xfsprogs 		xz
# Fri, 23 Sep 2016 16:39:44 GMT
RUN set -x 	&& addgroup -S dockremap 	&& adduser -S -G dockremap dockremap 	&& echo 'dockremap:165536:65536' >> /etc/subuid 	&& echo 'dockremap:165536:65536' >> /etc/subgid
# Fri, 23 Sep 2016 16:39:45 GMT
ENV DIND_COMMIT=3b5fac462d21ca164b3778647420016315289034
# Fri, 23 Sep 2016 16:39:45 GMT
RUN wget "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind" -O /usr/local/bin/dind 	&& chmod +x /usr/local/bin/dind
# Fri, 23 Sep 2016 16:39:46 GMT
COPY file:a00ae81495fdf69e63bb25e3b665aa29cb53cfe5788e6134adfc0f35caff6295 in /usr/local/bin/ 
# Fri, 23 Sep 2016 16:39:46 GMT
VOLUME [/var/lib/docker]
# Fri, 23 Sep 2016 16:39:47 GMT
EXPOSE 2375/tcp
# Fri, 23 Sep 2016 16:39:47 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Fri, 23 Sep 2016 16:39:47 GMT
CMD []
```

-	Layers:
	-	`sha256:c0cb142e43453ebb1f82b905aa472e6e66017efd43872135bc5372e4fac04031`  
		Last Modified: Fri, 23 Sep 2016 16:30:54 GMT  
		Size: 2.3 MB (2312930 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c6fe447e877c6fb78f7040d59f81a9aaac5be90ed3f7396a6dfd9aaa3467d29`  
		Last Modified: Fri, 23 Sep 2016 16:37:07 GMT  
		Size: 915.0 KB (915035 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e30628056ced332d91868633b4dd7b1e0d01c272aed22de32e75ab5d14527fa3`  
		Last Modified: Fri, 23 Sep 2016 16:39:07 GMT  
		Size: 28.8 MB (28846879 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4bbd10ee9f467ec4935446ab10e40b5d00c056becac1e3f90a93324cb5a1b6fb`  
		Last Modified: Fri, 23 Sep 2016 16:38:53 GMT  
		Size: 465.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d026e4545b650e9df67e0f04a5f5d07b22dda0203ee33b9a5205fe9ed6d80cb4`  
		Last Modified: Fri, 23 Sep 2016 16:39:55 GMT  
		Size: 2.1 MB (2065052 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6d15f585c97f7bfeda8fd87b3f4cac002586dec0ac6b4b03e88f5a890944132`  
		Last Modified: Fri, 23 Sep 2016 16:39:55 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:160b52153a252d7340bce1bb6317ee9ee3aea72eeda25198644f9b281cc3bfae`  
		Last Modified: Fri, 23 Sep 2016 16:39:54 GMT  
		Size: 1.8 KB (1821 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86b65c52178d55853598960b974b221925567ad4b593dfea2baae64d8ad2e001`  
		Last Modified: Fri, 23 Sep 2016 16:39:54 GMT  
		Size: 439.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
