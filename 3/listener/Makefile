CUR_DIR = $(shell pwd)

build:
	docker build -t "$$USER-listener-image" --progress=plain .
	docker run --rm -v ./:/workspace --entrypoint=colcon "$$USER-listener-image" build

run:
	docker run --rm -it --network=host --privileged -v /dev/shm:/dev/shm -v ./:/workspace "$$USER-listener-image"

.PHONY: run build