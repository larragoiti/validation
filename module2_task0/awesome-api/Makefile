build:
	go build

run:
	./awesome-api >./awesome.log 2>&1 &

stop:
	kill "$(pgrep awesome-api)"

clean:
	rm awesome-api awesome-api.log

test:
	curl http://localhost:9999
	curl http://localhost:9999/health

help:
	echo "help: ..."
