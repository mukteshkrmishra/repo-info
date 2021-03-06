## `python:2-windowsservercore`

```console
$ docker pull python@sha256:45b8ea8cbefa165c700e0d143382e593aff791aa07f37fc23fb0f586cbcc4745
```

-	Platforms:
	-	windows; amd64

### `python:2-windowsservercore` - windows; amd64

-	Docker Version: 1.12.0
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 GB (3529660092 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:38afc05150a7ab9d044d799345520e1d7710f246d3fe2db00c087b2737db7901`
-	Default Command: `["python"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Fri, 12 Aug 2016 17:01:50 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Thu, 18 Aug 2016 20:46:13 GMT
ENV PYTHON_VERSION=2.7.12
# Thu, 18 Aug 2016 20:46:16 GMT
ENV PYTHON_RELEASE=2.7.12
# Thu, 18 Aug 2016 21:45:53 GMT
ENV PYTHON_PIP_VERSION=8.1.2
# Thu, 18 Aug 2016 21:50:45 GMT
RUN $url = ('https://www.python.org/ftp/python/{0}/python-{1}.amd64.msi' -f $env:PYTHON_RELEASE, $env:PYTHON_VERSION); 	Write-Host ('Downloading {0} ...' -f $url); 	(New-Object System.Net.WebClient).DownloadFile($url, 'python.msi'); 		Write-Host 'Installing ...'; 	Start-Process msiexec -Wait 		-ArgumentList @( 			'/i', 			'python.msi', 			'/quiet', 			'/qn', 			'TARGETDIR=C:\Python', 			'ALLUSERS=1', 			'ADDLOCAL=DefaultFeature,Extensions,TclTk,Tools,PrependPath' 		); 		$env:PATH = [Environment]::GetEnvironmentVariable('PATH', [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  python --version'; python --version; 		Write-Host 'Removing ...'; 	Remove-Item python.msi -Force; 		$pipInstall = ('pip=={0}' -f $env:PYTHON_PIP_VERSION); 	Write-Host ('Installing {0} ...' -f $pipInstall); 	(New-Object System.Net.WebClient).DownloadFile('https://bootstrap.pypa.io/get-pip.py', 'get-pip.py'); 	python get-pip.py $pipInstall; 	Remove-Item get-pip.py -Force; 		Write-Host 'Verifying pip install ...'; 	pip --version; 		Write-Host 'Complete.';
# Thu, 18 Aug 2016 21:51:19 GMT
RUN pip install --no-cache-dir virtualenv
# Thu, 18 Aug 2016 21:51:23 GMT
CMD ["python"]
```

-	Layers:
	-	`sha256:1239394e5a8ab79fbd3b751dc5d98decf5886f14339958fdf5c1f96c89da58a7`  
		Size: 3.5 GB (3461145128 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:be0175dbdd12c150c89a273c6ae8a093858f186a1b130670b81917d39cfc62c3`  
		Last Modified: Tue, 16 Aug 2016 16:11:53 GMT  
		Size: 1.3 KB (1349 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05abb1fdc5e0a5854477cdc92e07d1a61c7d1b59a71be8628ee385d763efef27`  
		Last Modified: Mon, 22 Aug 2016 19:10:48 GMT  
		Size: 1.4 KB (1350 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f5506c423c9de332ab21eddb4e64514ce2d3bd20f1a6f3aac11e1657fa11b98`  
		Last Modified: Mon, 22 Aug 2016 19:10:42 GMT  
		Size: 1.4 KB (1353 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f2bd8a119c34b1fe5fe45b15a93c39d0c0e0044115c51086440abd0afa953e41`  
		Last Modified: Mon, 22 Aug 2016 19:10:42 GMT  
		Size: 1.4 KB (1355 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6498506e5667f24b429bdc954bc71f81cace762486ff573aa172776f4cea5c29`  
		Last Modified: Mon, 22 Aug 2016 19:11:24 GMT  
		Size: 60.9 MB (60889456 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1eb5f9260b1f007fc60814bdad74bf07f3577776a5b5167aad00bca639b3dc77`  
		Last Modified: Mon, 22 Aug 2016 19:10:48 GMT  
		Size: 7.6 MB (7618754 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:081ae10f91c676c05ca79f65d487e6a61ece777ca8b142890d612c32cb46e71c`  
		Last Modified: Mon, 22 Aug 2016 19:10:42 GMT  
		Size: 1.3 KB (1347 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
