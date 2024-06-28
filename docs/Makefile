BASE_URL ?= ""

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

build_existing_version: copyversion
	npm run build -- --baseurl $(BASE_URL)

debug: version
	npm run debug -- --baseurl $(BASE_URL)

version:
	(cd .. && make version)
	make copyversion

copyversion:
	cp -f ../.version ./_includes/.version
