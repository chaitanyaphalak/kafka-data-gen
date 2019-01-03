IMAGE_NAME?=kafkadatagen
IMAGE_VERSION?=$(shell git describe --tags | tr -d 'v')
HUB_REPO?=chaitanyaphalak

show_version:
	@echo ${IMAGE_VERSION}

docker: Dockerfile
	docker build --no-cache -t ${IMAGE_NAME}:${IMAGE_VERSION} .

tag: docker
	docker tag ${IMAGE_NAME}:${IMAGE_VERSION} ${HUB_REPO}/${IMAGE_NAME}:${IMAGE_VERSION}

push: tag
	docker push ${HUB_REPO}/${IMAGE_NAME}:${IMAGE_VERSION}

