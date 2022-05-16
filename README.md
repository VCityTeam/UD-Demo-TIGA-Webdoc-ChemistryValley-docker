# Dockerized UD-Demo-TIGA-Webdoc-ChemistryValley

This container wraps the [webdocumentary](https://github.com/VCityTeam/UD-Demo-TIGA-Webdoc-ChemistryValley) demo.

Build the docker image with

```bash
docker build -t vcity:webdoc .
```

no cache options :

```bash
docker build --no-cache -t vcity:webdoc .
```

If you want specify a branch name or commit name for UD-Demo-Anthropocene-GratteCiel use this

```bash
docker build -t vcity:webdoc --build-arg checkoutName=name .
```

no cache options :

```bash
docker build --no-cache -t vcity:webdoc --build-arg checkoutName=name .
```

Then run the container e.g. with

```bash
docker run [--detach] --rm -t vcity:webdoc
```

Run with redirection of port

```bash
docker run -p 0.0.0.0:8001:80 --detach --rm -t vcity:webdoc
```

and open a web browser on URL `http://localhost:8001/`

Note: in the above `docker run` command the optionnal `-d` argument requires the container to run in detached mode
