obj = main.o print_msg.o
CC = -O2 -march=native -std=c11

main: $(obj)
	gcc $(obj) $(CC) -o ../bin/print_msg

main.o: main.c 
	gcc main.c -c $(CC) -o main.o
 
print_msg.o: print_msg.c
	gcc print_msg.c -c $(CC) -o print_msg.o

clean:
	rm *.o
