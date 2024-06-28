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
	npm run build

debug: version
	npm run debug

version:
	(cd .. && make version)
	cp -f ../.version ./_includes/.version
