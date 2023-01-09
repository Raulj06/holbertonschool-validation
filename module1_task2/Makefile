build:	## builds the hugo website
	hugo

clean:	## cleans the content from dist directory
	rm -rf ./dist/*

post:	## adds posts
	hugo new posts/$(POST_NAME).md
	sed -i '2s/.*/title: "$(POST_TITLE)"/' content/posts/$(POST_NAME).md

.SILENT:
help:	## provides help about Makefile commands
	cat Makefile | grep '##' | tr -d '##'
