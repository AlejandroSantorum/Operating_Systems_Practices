CC = gcc -ansi -pedantic -std=c99
CFLAGS = -Wall -g
EXE = ejercicio2 ejercicio4 ejercicio6a ejercicio6b ejercicio9 prueba

all : $(EXE)

.PHONY : clean text
clean :
	rm -f *.o core $(EXE)
	
text :
	rm -f *.txt core $(EXE)

$(EXE) : % : %.o semaforos.o
	$(CC) $(CFLAGS) -o $@ $@.o -lm semaforos.o

semaforos.o : semaforos.c semaforos.h
	$(CC) $(CFLAGS) -c $<