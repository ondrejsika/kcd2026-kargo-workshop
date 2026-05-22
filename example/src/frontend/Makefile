IMAGE=ttl.sh/ondrejsikax/kcd2026-kargo-test/frontend
BUILD_ID=0

build-and-push-hello:
	docker build . \
		--build-arg BUILD_ID=${BUILD_ID} \
		-t ${IMAGE}:v${BUILD_ID}
	docker push ${IMAGE}:v${BUILD_ID}
