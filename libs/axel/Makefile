###########################
##   Makefile for Axel   ##
##                       ##
## Copyright 2001 Lintux ##
###########################

### DEFINITIONS

-include Makefile.settings

all: $(OUTFILE)

clean:
	rm -f *.o $(OUTFILE) search core *.mo

distclean: clean
	rm -f Makefile.settings config.h axel-*.tar axel-*.tar.gz axel-*.tar.bz2

### MAIN PROGRAM

$(OUTFILE): axel.o conf.o conn.o ftp.o http.o search.o tcp.o text.o
	$(CC) *.o -o $(OUTFILE) $(LFLAGS)
	$(STRIP) $(OUTFILE)

.c.o:
	$(CC) -c $*.c -o $*.o $(CFLAGS)
