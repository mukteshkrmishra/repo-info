## `mono:latest`

```console
$ docker pull mono@sha256:d72152d0f876176cfd895cdeda7d6b67692e90b2113bca3874146bebb8a76d02
```

-	Platforms:
	-	linux; amd64

### `mono:latest` - linux; amd64

-	Docker Version: 1.12.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **142.9 MB (142875794 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e5a4e90ac8a1dda8893f82170ae820b51f37268ea5247a605207eeb66e27be9f`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 19 Sep 2016 17:43:34 GMT
ADD file:b06eab13504d045bfba673dde1c6f5831a875e95146504a385baa101124f58f5 in / 
# Mon, 19 Sep 2016 17:43:35 GMT
CMD ["/bin/bash"]
# Mon, 19 Sep 2016 20:12:44 GMT
MAINTAINER Jo Shields <jo.shields@xamarin.com>
# Mon, 19 Sep 2016 21:05:34 GMT
RUN apt-get update   && apt-get install -y curl   && rm -rf /var/lib/apt/lists/*
# Mon, 19 Sep 2016 21:05:36 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF
# Wed, 21 Sep 2016 17:54:34 GMT
RUN echo "deb http://download.mono-project.com/repo/debian wheezy/snapshots/4.6.0.245 main" > /etc/apt/sources.list.d/mono-xamarin.list   && apt-get update   && apt-get install -y binutils mono-devel ca-certificates-mono fsharp mono-vbnc nuget referenceassemblies-pcl   && rm -rf /var/lib/apt/lists/* /tmp/*
```

-	Layers:
	-	`sha256:0fbab137f56aaa195d66eae971694eb98df3e4ff6a91eb4fa9905994ef40e5a1`  
		Last Modified: Mon, 19 Sep 2016 17:48:55 GMT  
		Size: 37.2 MB (37214522 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8fd4fae63c6a077b6d7e08b60cc62ac59c8674e444bf60eaaac99c8c202d4215`  
		Last Modified: Wed, 21 Sep 2016 18:10:58 GMT  
		Size: 7.6 MB (7554530 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:577c85bbb02e0673e738fb5e6e43a949778ca01877d1eb21ad13ecf754f31516`  
		Last Modified: Wed, 21 Sep 2016 18:10:57 GMT  
		Size: 29.3 KB (29330 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd0466fd115c268705db8b345b93c53d7da55719bb6001095ef65e1ff25c0f35`  
		Last Modified: Wed, 21 Sep 2016 18:15:39 GMT  
		Size: 98.1 MB (98077412 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
