build:	## hugo
	hugo
	go build -o awesome-api
	lint

run: ##  runs the application
	./awesome-api >./awesome.log 2>&1 &

clean:	## cleans the directory
	-pkill awesome-api
	rm -rf ./dist/*
	rm  -f ./awesome-api ./awesome.log

post:	## adds posts to website
	hugo new posts/$(POST_NAME).md
	sed -i '2s/.*/title: "$(POST_TITLE)"/' content/posts/$(POST_NAME).md

stop:	## stops the application
	pkill awesome-api

lint: ## lint
	golangci-lint run ./main.go


test: ## test behavior
	curl http://localhost:9999
	curl http://localhost:9999/health

.SILENT:
help:	## provides help
	cat Makefile | grep '##' | tr -d '##'
