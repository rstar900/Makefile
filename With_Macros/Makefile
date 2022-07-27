# Example Makefile (with macros)

# Macros
CAT_HOME = ${MGC_HOME}
TARGET_DIR = target
DEPENDS_DIR = include
SOURCE_DIR = src
TARGET = ${TARGET_DIR}/hello_main
OBJECTS = ${SOURCE_DIR}/main.o ${SOURCE_DIR}/hello.o
DEPENDS = ${DEPENDS_DIR}/hello.h
INCLUDES = -I"${DEPENDS_DIR}"
DEFINES = 
CXX = /usr/bin/g++
CXXFLAGS = -g -o3 ${DEFINES} ${INCLUDES}

# Main executable
${TARGET} : ${OBJECTS}
	${CXX} ${CXXFLAGS} -o ${TARGET} ${OBJECTS}

# For object files
${OBJECTS} : ${DEPENDS}

# phony target to remove all objects and executables
.PHONY : clean
clean:
	rm -f src/*.o 
	rm -f target/*
