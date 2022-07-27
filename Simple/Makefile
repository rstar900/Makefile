# Example Makefile (Simple version)

# Macros
CXX =  /usr/bin/g++
CXXFLAGS = -O

# hello_main (main executable)
hello_main : main.o hello.o
	${CXX} ${CXXFLAGS} -o hello_main main.o hello.o

# main.o
main.o : main.cpp hello.h
	${CXX} ${CXXFLAGS} -c main.cpp

# hello.o
hello.o : hello.cpp hello.h
	${CXX} ${CXXFLAGS} -c hello.cpp

# phony target to remove all objects and executables
.PHONY : clean
clean:
	rm -f *.o *.exe

