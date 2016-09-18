CC=gcc

LIBJPEG=libjpeg6 libjpeg6-turbo libjpeg7-turbo libjpeg8-turbo

libjpeg6_PREFIX=/usr
libjpeg6-turbo_PREFIX=/usr/lib/libjpeg6-turbo
libjpeg7-turbo_PREFIX=/usr/lib/libjpeg7-turbo
libjpeg8-turbo_PREFIX=/usr/lib/libjpeg8-turbo

run:
	@mkdir bin; \
	for lib in $(LIBJPEG); \
	do \
		prefix=$($${lib}_PREFIX); \
		incdir=$$lib/include; \
		bindir=$$lib/bin; \
		libdir=$$lib/lib; \
		echo $$bindir; \
		CC=$(CC) CFLAGS="-I$$incdir" LDFLAGS="-L$$libdir -R$$libdir" \
		SUFFIX="_$$lib" \
		make -C src; \
	done;
