COMPILER=g++
DEBUG=gdb
CFLAGS=-O2
DEFLAGS=-g -Wall -Wextra --pedantic-errors
SOURCES=$(wildcard *.cpp)
HEADERS=$(wildcard*.h)
OBJECTS=$(SOURCES:%.cpp=%.o)

default: triangles
triangles: $(OBJECTS)
	$(COMPILER) ${CFLAGS} $(OBJECTS) -o triangles
.PHONY: debug clean
debug: CFLAGS=${DEFLAGS}
debug: triangles

%.o: %.cpp $(HEADERS)
	$(COMPILER) -c $(CFLAGS) $<
clean:
	-@ rm -f triangles
	-@ rm -f $(OBJECTS)