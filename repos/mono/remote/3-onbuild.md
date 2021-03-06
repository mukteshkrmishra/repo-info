## `mono:3-onbuild`

```console
$ docker pull mono@sha256:8f69b919bafa772e104a437c2b565e0b6a95ee7fdc492264f4e56e366e4a2df1
```

-	Platforms:
	-	linux; amd64

### `mono:3-onbuild` - linux; amd64

-	Docker Version: 1.12.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **125.6 MB (125600474 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dcc4e47a6ff1c888f1453d5c13bbc8c66704b896130152ec42992814cb42a092`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 19 Sep 2016 17:43:34 GMT
ADD file:b06eab13504d045bfba673dde1c6f5831a875e95146504a385baa101124f58f5 in / 
# Mon, 19 Sep 2016 17:43:35 GMT
CMD ["/bin/bash"]
# Mon, 19 Sep 2016 20:12:44 GMT
MAINTAINER Jo Shields <jo.shields@xamarin.com>
# Mon, 19 Sep 2016 20:12:53 GMT
RUN apt-get update 	&& apt-get install -y curl 	&& rm -rf /var/lib/apt/lists/*
# Mon, 19 Sep 2016 20:12:55 GMT
RUN apt-key adv --keyserver pgp.mit.edu --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF
# Mon, 19 Sep 2016 20:14:56 GMT
RUN echo "deb http://download.mono-project.com/repo/debian wheezy/snapshots/3.12.0 main" > /etc/apt/sources.list.d/mono-xamarin.list         && echo "deb http://download.mono-project.com/repo/debian 312-security main" >> /etc/apt/sources.list.d/mono-xamarin.list 	&& apt-get update 	&& apt-get install -y mono-devel ca-certificates-mono fsharp mono-vbnc nuget 	&& rm -rf /var/lib/apt/lists/*
# Mon, 19 Sep 2016 20:14:56 GMT
MAINTAINER Jo Shields <jo.shields@xamarin.com>
# Mon, 19 Sep 2016 20:14:57 GMT
RUN mkdir -p /usr/src/app/source /usr/src/app/build
# Mon, 19 Sep 2016 20:14:57 GMT
WORKDIR /usr/src/app/source
# Mon, 19 Sep 2016 20:14:58 GMT
ONBUILD COPY . /usr/src/app/source
# Mon, 19 Sep 2016 20:14:58 GMT
ONBUILD RUN nuget restore -NonInteractive
# Mon, 19 Sep 2016 20:14:58 GMT
ONBUILD RUN xbuild /property:Configuration=Release /property:OutDir=/usr/src/app/build/
# Mon, 19 Sep 2016 20:14:58 GMT
ONBUILD WORKDIR /usr/src/app/build
```

-	Layers:
	-	`sha256:0fbab137f56aaa195d66eae971694eb98df3e4ff6a91eb4fa9905994ef40e5a1`  
		Last Modified: Mon, 19 Sep 2016 17:48:55 GMT  
		Size: 37.2 MB (37214522 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4108b1bf47289b169ca3592a05ab76964fcdd284dea1d08d23825d8ca6e81179`  
		Last Modified: Wed, 21 Sep 2016 17:54:49 GMT  
		Size: 7.6 MB (7554528 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1976f254995345b055384d35cd86b4316054404f380d9509d6e1650338faccfe`  
		Last Modified: Wed, 21 Sep 2016 17:54:47 GMT  
		Size: 29.3 KB (29328 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65712670119ab4e92788d7735fd31c186e291329acfb78c0dfc60b68025a7ccf`  
		Last Modified: Wed, 21 Sep 2016 17:56:32 GMT  
		Size: 80.8 MB (80801932 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef7d13d9db6d6c8ba4a62a3a530540117640265d65a5bb196e7dcb312d193ab9`  
		Last Modified: Wed, 21 Sep 2016 17:57:16 GMT  
		Size: 164.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
