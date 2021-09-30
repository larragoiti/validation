# Add the following 'help' target to your Makefile
# And add help text after each target name starting with '\#\#'
 
help:           ## Show this help.
	@fgrep -h "##" $(MAKEFILE_LIST) | fgrep -v fgrep | sed -e 's/\\$$//' | sed -e 's/##//'

build: ## Build
	go build

run: ## Run
	./awesome-api >./awesome.log 2>&1 &

stop: ##stop
	kill -9 $$(pgrep awesome-api)

clean: ## clean
	rm -f awesome-api awesome.log
	kill -9 $$(pgrep awesome-api)

test: ## test
	curl http://localhost:9999 && curl http://localhost:9999/health

lint: ## Lint
	golangci-lint run

