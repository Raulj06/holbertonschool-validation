build: ## build hugo
	hugo

clean: ## erase the content from directory
	rm -rf ./dist/*

post: ## creates a post
	hugo new posts/$(POST_NAME).md
	sed -i '2s/.*/title: "$(POST_TITLE)"/' content/posts/$(POST_NAME).md
.SILENT:
help:	## provides help about commands
	cat Makefile | grep '##' | tr -d '##'
