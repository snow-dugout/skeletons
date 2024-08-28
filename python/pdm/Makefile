.PHONY: fmt
fmt:
	pdm fmt

.PHONY: lint
lint:
	pdm lint

.PHONY: test
test:
	pdm test

.PHONY: init
init:
	pipx ensurepath
	pipx install pdm
	pipx install pre-commit

.PHONY: build-image
build-image:
	docker buildx build -t snow-dugout/skeletons:python-pdm --no-cache --push \
		-f docker/Dockerfile \
		.