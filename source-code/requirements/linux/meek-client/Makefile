DESTDIR =
PREFIX = /usr/local
BINDIR = $(PREFIX)/bin

GOBUILDFLAGS =
ENV = GOOS=linux GOARCH=arm64

all: meek-client

meek-client: *.go
	$(ENV) go build $(GOBUILDFLAGS)

install: meek-client
	mkdir -p "$(DESTDIR)$(BINDIR)"
	cp -f meek-client "$(DESTDIR)$(BINDIR)"

clean:
	rm -f meek-client

fmt:
	go fmt

.PHONY: all install clean fmt
