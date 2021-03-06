## `kong:latest`

```console
$ docker pull kong@sha256:d4dff535ea9c2fa29ae007ca6e7d20c7e2dd563db8ea45f52d7812aacd1c0087
```

-	Platforms:
	-	linux; amd64

### `kong:latest` - linux; amd64

-	Docker Version: 1.12.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **132.2 MB (132248844 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b01bd6e3f2ce5c18665ef97b6982b1fff11feaac13929d72f1e5e69272daa41c`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","start"]`

```dockerfile
# Tue, 30 Aug 2016 18:18:45 GMT
MAINTAINER https://github.com/CentOS/sig-cloud-instance-images
# Tue, 06 Sep 2016 21:10:17 GMT
ADD file:e336b45186086f7d9d9b8e8be3d6c027bc9c14dbfdde2bb056793ee458bd1a57 in / 
# Tue, 06 Sep 2016 21:10:19 GMT
LABEL name=CentOS Base Image vendor=CentOS license=GPLv2 build-date=20160906
# Tue, 06 Sep 2016 21:10:20 GMT
CMD ["/bin/bash"]
# Tue, 06 Sep 2016 21:17:41 GMT
MAINTAINER Marco Palladino, marco@mashape.com
# Wed, 21 Sep 2016 17:53:29 GMT
ENV KONG_VERSION=0.9.2
# Wed, 21 Sep 2016 17:54:02 GMT
RUN yum install -y wget https://github.com/Mashape/kong/releases/download/$KONG_VERSION/kong-$KONG_VERSION.el7.noarch.rpm &&     yum clean all
# Wed, 21 Sep 2016 17:54:05 GMT
RUN wget -O /usr/local/bin/dumb-init https://github.com/Yelp/dumb-init/releases/download/v1.1.3/dumb-init_1.1.3_amd64 &&     chmod +x /usr/local/bin/dumb-init
# Wed, 21 Sep 2016 17:54:06 GMT
COPY file:324f2e5f56829733b3c3c8b6971998202fa01bf7368caac6c1971fcec0464e8c in /docker-entrypoint.sh 
# Wed, 21 Sep 2016 17:54:07 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 21 Sep 2016 17:54:08 GMT
EXPOSE 7946/tcp 8000/tcp 8001/tcp 8443/tcp
# Wed, 21 Sep 2016 17:54:09 GMT
CMD ["kong" "start"]
```

-	Layers:
	-	`sha256:8d30e94188e7f13642d975e70c484e48c33867f3ede3277df1145803fa996ac1`  
		Last Modified: Tue, 06 Sep 2016 21:10:57 GMT  
		Size: 70.6 MB (70591526 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:854d44197af65395dd090883606f2f91c39d81550e071b72246ff1db5fd8a2d3`  
		Last Modified: Wed, 21 Sep 2016 17:54:31 GMT  
		Size: 61.6 MB (61632433 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:918904393ef5ed4907d00d636d13c9a6fcde407fe6dcec586cc7f1c4cf8a993b`  
		Last Modified: Wed, 21 Sep 2016 17:54:14 GMT  
		Size: 24.6 KB (24646 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cec439ba9a68abd74fdc76d68663e0611829d1676065261489c8a64caa2769fc`  
		Last Modified: Wed, 21 Sep 2016 17:54:15 GMT  
		Size: 239.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
