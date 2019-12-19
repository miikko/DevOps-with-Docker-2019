Project taken from exercise 1.13

Image sizes:

* Old: 574MB
* New: 190MB

## Build

`$  docker build -t spring-example-(old/new) -f Dockerfile-(old/new) .`

## Run

`docker run -it --rm -p 8080:8080 spring-example-(old/new)`
