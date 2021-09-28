# Add the following 'help' target to your Makefile
# And add help text after each target name starting with '\#\#'
 
help:           ## Show this help.
	@fgrep -h "##" $(MAKEFILE_LIST) | fgrep -v fgrep | sed -e 's/\\$$//' | sed -e 's/##//'

build: ## Build
	go build

run: ## Run
	./awesome-api >./awesome.log 2>&1 &

stop: ##stop
	kill $$(pgrep awesome-api)

clean: ## clean
	rm -f awesome*

test: ## test
	curl http://localhost:9999 && curl http://localhost:9999/health

