SHELL=/bin/sh

DPKG_EXPORT_BUILDFLAGS = 1
include /usr/share/dpkg/buildflags.mk

CC=gcc
CFLAGS+=-O2 -Wall -Wextra

PROG=gti
PREFIX=$(DESTDIR)/usr/games

$(PROG): *.c
	$(CC) -o $@ $(CPPFLAGS) $(CFLAGS) $(LDFLAGS) $^

install: $(PROG)
	mkdir -p $(PREFIX)
	cp $^ $(PREFIX)

uninstall:
	rm -f $(PREFIX)/$(PROG)

.PHONY: clean install uninstall
clean:
	rm -f $(PROG)

