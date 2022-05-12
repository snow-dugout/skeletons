# Python Skeleton

## Develop or Contribution

### Run Black using Docker
```shell
docker run -it --rm --entrypoint='black' -v $(pwd):/opt/project -w /opt/project ghcr.io/loustler/skeletons:python-3.9 .
```
