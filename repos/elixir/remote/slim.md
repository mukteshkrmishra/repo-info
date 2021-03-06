## `elixir:slim`

```console
$ docker pull elixir@sha256:9c282a1adfa70c9476695a9e879fa4812867d135c66c26838d5f3daee08397e3
```

-	Platforms:
	-	linux; amd64

### `elixir:slim` - linux; amd64

-	Docker Version: 1.12.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **120.6 MB (120640817 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e4b157feb043a5998a8c948155e5824f38e3302780840e7bbb6bf96d4f44df3d`
-	Default Command: `["iex"]`

```dockerfile
# Fri, 23 Sep 2016 18:08:50 GMT
ADD file:c6c23585ab140b0b320d4e99bc1b0eb544c9e96c24d90fec5e069a6d57d335ca in / 
# Fri, 23 Sep 2016 18:08:51 GMT
CMD ["/bin/bash"]
# Fri, 23 Sep 2016 18:57:46 GMT
ENV OTP_VERSION=19.1
# Fri, 23 Sep 2016 19:03:24 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="caf320c07bdd4c6e11831a0b0d25645a29112007077dbf11eec22437f8b041ed" 	&& runtimeDeps=' 		libodbc1 		libssl1.0.0 		libsctp1 	' 	&& buildDeps=' 		curl 		ca-certificates 		autoconf 		gcc 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256 otp-src.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/src/otp-src 	&& tar -xzf otp-src.tar.gz -C /usr/src/otp-src --strip-components=1 	&& rm otp-src.tar.gz 	&& cd /usr/src/otp-src 	&& ./otp_build autoconf 	&& ./configure --enable-sctp 	&& make -j$(nproc) 	&& make install 	&& find /usr/local -name examples | xargs rm -rf 	&& apt-get purge -y --auto-remove $buildDeps 	&& rm -rf /usr/src/otp-src /var/lib/apt/lists/*
# Fri, 23 Sep 2016 19:03:25 GMT
CMD ["erl"]
# Tue, 27 Sep 2016 17:38:15 GMT
ENV ELIXIR_VERSION=v1.3.3 LANG=C.UTF-8
# Tue, 27 Sep 2016 17:38:32 GMT
RUN set -xe 	&& ELIXIR_DOWNLOAD_URL="https://github.com/elixir-lang/elixir/releases/download/${ELIXIR_VERSION}/Precompiled.zip" 	&& ELIXIR_DOWNLOAD_SHA256="afb5a7437c3dc9ed40d355de045bd21a136eba6be213e3be48bc1ab1d7550ad4" 	&& buildDeps=' 		ca-certificates 		curl 		unzip 	' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $buildDeps 	&& curl -fSL -o elixir-precompiled.zip $ELIXIR_DOWNLOAD_URL 	&& echo "$ELIXIR_DOWNLOAD_SHA256 elixir-precompiled.zip" | sha256sum -c - 	&& unzip -d /usr/local elixir-precompiled.zip 	&& rm elixir-precompiled.zip 	&& apt-get purge -y --auto-remove $buildDeps 	&& rm -rf /var/lib/apt/lists/*
# Tue, 27 Sep 2016 17:38:33 GMT
CMD ["iex"]
```

-	Layers:
	-	`sha256:6a5a5368e0c2d3e5909184fa28ddfd56072e7ff3ee9a945876f7eee5896ef5bb`  
		Last Modified: Fri, 23 Sep 2016 18:10:19 GMT  
		Size: 51.4 MB (51354364 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31fd23e4495196d140bf6b83740e2fcdffad4094a73adb4b60ad6a71e3bd1361`  
		Last Modified: Fri, 23 Sep 2016 19:03:47 GMT  
		Size: 65.5 MB (65547900 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6bb00ccc550fa6d3bf2b44a0a47dab20c903ab1fa99524737948ff29711c980b`  
		Last Modified: Tue, 27 Sep 2016 17:39:18 GMT  
		Size: 3.7 MB (3738553 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
