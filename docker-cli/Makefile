VERSION := 1.0.0

.PHONY: build
build:
	docker buildx build --platform linux/arm64/v8,linux/amd64 --load --tag ourskyci/docker-cli:$(VERSION) .

.PHONY: push
push:
	docker buildx build --platform linux/arm64/v8,linux/amd64 --push --tag ourskyci/docker-cli:$(VERSION) .

.PHONY: push-latest
push-latest:
	$(MAKE) push VERSION=latest
