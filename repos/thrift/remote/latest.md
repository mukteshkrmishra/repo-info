## `thrift:latest`

```console
$ docker pull thrift@sha256:7f5e8f81d9e0d59792cb8039c150f29feda25fd285a974e06bce1a00881d37e0
```

-	Platforms:
	-	linux; amd64

### `thrift:latest` - linux; amd64

-	Docker Version: 1.12.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.1 MB (49087615 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8c441d15e2302e9b525a5fcfb0ceda5f184211f6af568b9dd09ee9c7c9a1b936`
-	Default Command: `["thrift"]`

```dockerfile
# Mon, 19 Sep 2016 17:43:34 GMT
ADD file:b06eab13504d045bfba673dde1c6f5831a875e95146504a385baa101124f58f5 in / 
# Mon, 19 Sep 2016 17:43:35 GMT
CMD ["/bin/bash"]
# Tue, 20 Sep 2016 00:45:30 GMT
MAINTAINER Adam Hawkins <adam@hawkins.io>
# Tue, 20 Sep 2016 00:45:30 GMT
ENV THRIFT_VERSION=0.9.3
# Tue, 20 Sep 2016 00:49:56 GMT
RUN buildDeps=" 		automake 		bison 		curl 		flex 		g++ 		libboost-dev 		libboost-filesystem-dev 		libboost-program-options-dev 		libboost-system-dev 		libboost-test-dev 		libevent-dev 		libssl-dev 		libtool 		make 		pkg-config 	"; 	apt-get update && apt-get install -y --no-install-recommends $buildDeps && rm -rf /var/lib/apt/lists/* 	&& curl -sSL "http://apache.mirrors.spacedump.net/thrift/$THRIFT_VERSION/thrift-$THRIFT_VERSION.tar.gz" -o thrift.tar.gz 	&& mkdir -p /usr/src/thrift 	&& tar zxf thrift.tar.gz -C /usr/src/thrift --strip-components=1 	&& rm thrift.tar.gz 	&& cd /usr/src/thrift 	&& ./configure  --without-python --without-cpp 	&& make 	&& make install 	&& cd / 	&& rm -rf /usr/src/thrift 	&& curl -k -sSL "https://storage.googleapis.com/golang/go1.4.linux-amd64.tar.gz" -o go.tar.gz 	&& tar xzf go.tar.gz 	&& rm go.tar.gz 	&& cp go/bin/gofmt /usr/bin/gofmt 	&& rm -rf go 	&& apt-get purge -y --auto-remove $buildDeps
# Tue, 20 Sep 2016 00:49:56 GMT
CMD ["thrift"]
```

-	Layers:
	-	`sha256:0fbab137f56aaa195d66eae971694eb98df3e4ff6a91eb4fa9905994ef40e5a1`  
		Last Modified: Mon, 19 Sep 2016 17:48:55 GMT  
		Size: 37.2 MB (37214522 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e4a6fb7650817ec8ed7bd301da34b859b955944c1d2167877a02b8a4c1fada3`  
		Last Modified: Fri, 23 Sep 2016 23:44:02 GMT  
		Size: 11.9 MB (11873093 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
