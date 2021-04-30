CC = g++
FLAGS = -std=c++17 -Wall -Werror -Wextra -Wpedantic -Wno-unused-variable
VPATH = src:lib
OBJECTS = PPlot.o SVGPainter.o test.o main.o 

assignment12: $(OBJECTS)
	$(CC) $(OBJECTS) -o assignment12

debug: FLAGS += -g
debug: assignment11

PPlot.o: PPlot.cpp PPlot.h
	$(CC) $(FLAGS) -c lib/PPlot.cpp

SVGPainter.o: SVGPainter.cpp SVGPainter.h
	$(CC) $(FLAGS) -c lib/SVGPainter.cpp

test.o: test.cpp PriorityQueue.h timing.h
	$(CC) $(FLAGS) -Ilib -c src/test.cpp

main.o: main.cpp PriorityQueue.h timing.h
	$(CC) $(FLAGS) -Ilib -c src/main.cpp

clean:
	rm assignment12 *.o *.svg
