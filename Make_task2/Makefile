all: executable

include make1.mk
include make2.mk
# intentionally, so i can use `make -f`

executable: sources main.o
	gcc -o $@ *.o

main.o: main.c
	gcc -c $< -o $@
	
sources: src1.o src2.o src3.c
	make -f make3.mk src3.o
	
clean: 
	rm -f *.o
	rm -f executable