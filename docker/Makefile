.PHONY: build
build:
	docker buildx build --platform linux/arm64/v8,linux/amd64 --load --tag ourskyci/docker:dind .

.PHONY: push
push:
	docker buildx build --platform linux/arm64/v8,linux/amd64 --push --tag ourskyci/docker:dind .
