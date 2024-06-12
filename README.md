#### Python GDAL PROJ Docker Image
NOTE: due to not being able to name the image dynamically in Github action, using manual:
1. export CR_PAT=YOUR_PAT
2. echo $CR_PAT | docker login ghcr.io -u trimbleava --password-stdin
3. docker build . -f Dockerfile.gdal -t ghcr.io/trimbleava/dockers/py10-gdal3.8.5:v1
4. docker push ghcr.io/trimbleava/dockers/py10-gdal3.8.5:v1
5. display packages: https://github.com/users/trimbleava/packages/container/package/
6. docker pull ghcr.io/trimbleava/dockers/py10-gdal3.8.5:v1

```bash
$ docker build . -t py10-gdal3.8.5:v1
```

Will output Python, pip and GDAL versions:

```console
Python 3.10.0
pip 21.2.4 from /usr/local/lib/python3.10/site-packages/pip (python 3.10)
GDAL 3.8.5, released 2021/04/27
```

Run container and start an interactive bash session as root

```bash
$ docker run -it trimbleava/dockers/py10-gdal3.8.5:v1 bash
```