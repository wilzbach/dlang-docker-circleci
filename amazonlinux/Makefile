BASE_IMAGE="amazonlinux:1"
DOCKER_POSTFIX=-amazonlinux

include ../common.mak

Dockerfile: dlang.docker Makefile
	cat $< | \
		sed "s|{{D_VERSION}}|${D_VERSION_RESOLVED}|g" | \
		sed "s|{{BASE_IMAGE}}|${BASE_IMAGE}|g" | \
		sed "s|{{BIN_FOLDER}}|${BIN_FOLDER}|g" | \
		sed "s|{{LIB_FOLDER}}|${LIB_FOLDER}|g" \
		> $@

clean:
	rm Dockerfile
