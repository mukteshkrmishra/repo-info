## `docker:1-experimental-git`

```console
$ docker pull docker@sha256:5cf5290269a6571dc6d98f8ea6c1ac61a972da83a15d6bd925f27b3359290653
```

-	Platforms:
	-	linux; amd64

### `docker:1-experimental-git` - linux; amd64

-	Docker Version: 1.12.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **41.2 MB (41211203 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8773ee253ac5ab6c0c922dc7b6c08bf335c0f874cf06c35daa65463eb17fc669`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Mon, 19 Sep 2016 23:24:18 GMT
ADD file:fd71807f3b22f7f51f502e8aed6bd23067e6822ae08dec31e7477044d770cf48 in / 
# Mon, 19 Sep 2016 23:48:30 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl
# Mon, 19 Sep 2016 23:51:41 GMT
ENV DOCKER_BUCKET=experimental.docker.com
# Mon, 19 Sep 2016 23:51:42 GMT
ENV DOCKER_VERSION=1.12.1
# Mon, 19 Sep 2016 23:51:42 GMT
ENV DOCKER_SHA256=f92fe0630dd1f20d9678cd7e4043018566e3737001f53171274a4a6ed6baaa08
# Mon, 19 Sep 2016 23:51:46 GMT
RUN set -x 	&& curl -fSL "https://${DOCKER_BUCKET}/builds/Linux/x86_64/docker-${DOCKER_VERSION}.tgz" -o docker.tgz 	&& echo "${DOCKER_SHA256} *docker.tgz" | sha256sum -c - 	&& tar -xzvf docker.tgz 	&& mv docker/* /usr/local/bin/ 	&& rmdir docker 	&& rm docker.tgz 	&& docker -v
# Mon, 19 Sep 2016 23:51:47 GMT
COPY file:50006c902e7677711aeffe4ab7b7042d649618b96dec760f322a8566dd83ab25 in /usr/local/bin/ 
# Mon, 19 Sep 2016 23:51:47 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 19 Sep 2016 23:51:47 GMT
CMD ["sh"]
# Mon, 19 Sep 2016 23:53:39 GMT
RUN apk add --no-cache 		git 		openssh-client
```

-	Layers:
	-	`sha256:117f30b7ae3d50ac80e38e390a39f70848edcfc916127c2821604a8114c080aa`  
		Last Modified: Mon, 19 Sep 2016 23:25:22 GMT  
		Size: 2.3 MB (2311053 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64f1b7d4bfe4e9782e02d9870a81f91a195e15eb9bf2b55486799e4b113576b1`  
		Last Modified: Mon, 19 Sep 2016 23:48:45 GMT  
		Size: 914.3 KB (914310 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f29694a1cc2c0bc22ca2498707a882b6f7baab029c774658da3deeeeaa30f558`  
		Last Modified: Mon, 19 Sep 2016 23:52:11 GMT  
		Size: 28.8 MB (28846877 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69d5cee0f926515b2595ed32d4fd93a29307a4efddb5ac056e13cc180b7ff328`  
		Last Modified: Mon, 19 Sep 2016 23:51:55 GMT  
		Size: 465.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96daf78963bc9d6f97e57399e04755d2d01f120a6ebacdc1f3c3b712e92ee9d3`  
		Last Modified: Mon, 19 Sep 2016 23:53:49 GMT  
		Size: 9.1 MB (9138498 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
