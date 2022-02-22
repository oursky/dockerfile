VERSION := 1.0.0

.PHONY: build
build:
	docker buildx build --platform linux/arm64/v8,linux/amd64 --load --tag ourskyci/dind:$(VERSION) .

.PHONY: push
push:
	docker buildx build --platform linux/arm64/v8,linux/amd64 --push --tag ourskyci/dind:$(VERSION) .
