BENCHMARKS=\
	bfs \
	fft \
	gemm \
	md-grid \
	md-knn \
	mergesort \
	nw \
	spmv \
	stencil2d \
	stencil3d

CFLAGS=-O1 -Wall -Wno-unused-label

.PHONY: build clean all

build:
	@( for b in $(BENCHMARKS); do $(MAKE) CFLAGS="$(CFLAGS)" -C $$b; done )

clean:
	@( for b in $(BENCHMARKS); do $(MAKE) -C $$b clean || exit ; done )

all: clean build
