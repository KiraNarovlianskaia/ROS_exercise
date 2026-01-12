CUR_DIR = $(shell pwd)

build:
	docker build -t "$$USER-publisher-image" --progress=plain .
	docker run --rm -v ./:/workspace --entrypoint=colcon "$$USER-publisher-image" build

run:
	docker run --rm -it --network=host --privileged -v /dev/shm:/dev/shm -v ./:/workspace "$$USER-publisher-image"

.PHONY: run build