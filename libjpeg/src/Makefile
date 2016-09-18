BINDIR=../bin

all:
	${CC} libjpeg_bench.c -o bench${SUFFIX} ${CFLAGS} -std=c99 ${LDFLAGS} -ljpeg
	mkdir -p $(BINDIR) 
	mv bench${SUFFIX} $(BINDIR) 
