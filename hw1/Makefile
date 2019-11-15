CC = gcc
CFLAGS = -O2 -Wall -I .

# This flag includes the Pthreads library on a Linux box.
# Others systems will probably require something different.
LIB = -lpthread

all: hw01 cgi

hw01: hw01.c csapp.o
	$(CC) $(CFLAGS) -o hw01 hw01.c csapp.o $(LIB)

csapp.o: csapp.c
	$(CC) $(CFLAGS) -c csapp.c

cgi:
	(cd cgi-bin; make)

clean:
	rm -f *.o hw01 *~
	(cd cgi-bin; make clean)

