.PHONY: help docker-start docker-stop ## The target is not a real file

.DEFAULT_GOAL = help

help: ## Displays all the commands make
	@grep -E '(^[a-zA-Z_-]+:.*?##.*$$)|(^##)' $(MAKEFILE_LIST) | awk 'BEGIN {FS = ":.*?## "}; {printf "\033[32m%-10s\033[0m %s\n", $$1, $$2}' | sed -e 's/\[32m##/[33m/'

docker-start: ## Run the containers and build them if they are not, remove containers which were created in a previous run and recreate them
	docker stop $$(docker container ls -aq)
	docker-compose up -d --build --remove-orphans --force-recreate

docker-stop: ## Stop all containers
	docker stop $$(docker container ls -aq)
