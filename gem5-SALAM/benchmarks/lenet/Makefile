FOLDERS=channel_unroll kernel_unroll no_unroll

.PHONY: build clean all

build:
	@( for f in $(FOLDERS); do $(MAKE) CFLAGS="$(CFLAGS)" -C $$f; done )

clean:
	@( for f in $(FOLDERS); do $(MAKE) -C $$f clean || exit ; done )

all: clean build
