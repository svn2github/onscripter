#
# Makefile for installing the Mingw32 version of the SDL library

all:
	if test -d $(prefix); then \
	    cp -rv bin lib $(prefix)/; \
	    mkdir $(prefix)/include/SDL; \
	    cp -v include/SDL/* $(prefix)/include/SDL; \
	    sed "s|^prefix=.*|prefix=$(prefix)|" <bin/sdl-config >$(prefix)/bin/sdl-config; \
	    chmod 755 $(prefix)/bin/sdl-config; \
	    sed "s|^libdir=.*|libdir=\'$(prefix)/lib\'|" <lib/libSDL.la >$(prefix)/lib/libSDL.la; \
	else \
	    echo "*** ERROR: $(prefix) does not exist!"; \
	    exit 1; \
	fi
