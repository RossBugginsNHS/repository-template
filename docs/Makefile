BASE_URL ?= "/"
VERSION ?= ""
SHELL = /bin/bash

default: install

h help:
	@egrep '^\S|^$$' Makefile

install:
	bundle config set --local path vendor/bundle
	bundle install
	npm install

s serve:
	bundle exec jekyll serve --trace --livereload

build: version
	npm run build -- --baseurl $(BASE_URL)

debug: version
	npm run debug -- --baseurl $(BASE_URL)

version:
	touch _config.version.yml
	if [[ $(VERSION) == "" ]]; then \
		(cd .. && make version); \
		ver=$$(head -n 1 ../.version 2> /dev/null || echo unknown); \
		echo "version: $$ver" > _config.version.yml; \
	else \
		echo "version: $(VERSION)" > _config.version.yml; \
	fi

