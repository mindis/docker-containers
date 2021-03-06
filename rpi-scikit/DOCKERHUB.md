# Purpose

A container with Python 3.7 + Scikit-Learn + Jupyter Lab for use with Raspberry Pi 4 (armv7l).

Note that you should be building and using this container only on a Raspberry Pi 4.

# Source

[GitHub](https://github.com/oneoffcoder/docker-containers/tree/master/rpi-scikit)

# Docker

Pull it.

```bash
docker pull oneoffcoder/rpi-scikit:latest
```

Run it (plain).

```bash
docker run -it -p 8888:8888 oneoffcoder/rpi-scikit
```

Run it (with host mount).

```bash
docker run -it \
    -p 8888:8888 \
    -v /home/pi/git/docker-containers/rpi-scikit/ipynb:/ipynb \
    oneoffcoder/rpi-scikit
```

Run it (with Jupyter Notebook instead of Jupyter lab)

```bash
docker run -it \
    -p 8888:8888 \
    -v /home/pi/git/docker-containers/rpi-scikit/ipynb:/ipynb \
    -e JUPYTER_TYPE=notebook \
    oneoffcoder/rpi-scikit
```

Observe it.

* [http://localhost:8888](http://localhost:8888)