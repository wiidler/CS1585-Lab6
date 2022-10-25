
default: triangles
triangles: main.o funcs.o TrianglePrinter.o
	g++ main.o funcs.o TrianglePrinter.o -o triangles
main.o: main.cpp funcs.h TrianglePrinter.h
	g++ -c main.cpp
TrianglePrinter.o: TrianglePrinter.cpp TrianglePrinter.h
	g++ -c TrianglePrinter.cpp
funcs.o: funcs.cpp funcs.h
	g++ -c funcs.cpp
.PHONY: clean
clean:
	-rm -f triangles *.o