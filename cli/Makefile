.PHONY: dist

all: build

build:
	go build ${ARGS} bitcart-cli.go

dist:
	go install github.com/mitchellh/gox@master
	gox -osarch '!darwin/386' -output "dist/bitcart-cli-{{.OS}}-{{.Arch}}" ${ARGS}

release: clean dist

clean:
	rm -f bitcart-cli dist/bitcart-cli-*
