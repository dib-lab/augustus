#	Makefile for filterBam.cc and filterBam.tex
#	
# 	Created: 28-February-2012
#	Last modified: 15-October-2015

INCLUDES =  ${PREFIX}/include/bamtools/
LIBS = ${PREFIX}/lib/libbamtools.a -lz
SOURCES = bam2hints.cc
OBJECTS = $(SOURCES:.cc=.o)
CFLAGS = -Wall -g -p -O0
CXXFLAGS += -Wall -O2 # -g -p -g -ggdb 

all: 
	(cd src;make CXX=$(BAMTOOLS_CXX) CC=$(BAMTOOLS_CC))

clean:
	(cd src; make clean; cd ../bin; rm -f filterBam; cd ../../../bin; rm -f filterBam)
