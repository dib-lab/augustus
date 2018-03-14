#	Makefile for filterBam
#	
#	Created: 11-November-2011
#	Last modified: 4-March-2012


SOURCES = filterBam.cc MatePairs.cc getReferenceName.cc initOptions.cc SingleAlignment.cc \
			printElapsedTime.cc sumMandIOperations.cc sumDandIOperations.cc PairednessCoverage.cc
PROGRAM = filterBam
OBJECTS = $(SOURCES:.cc=.o)
INCLUDES =  -I${PREFIX}/include/bamtools/ -Iheaders -I./bamtools
LIBS = $(PREFIX)/lib/libbamtools.a -lz
CFLAGS += -std=c++11 -Wall -O2 # -g -p -g -ggdb
VPATH = functions 
INSTDIR = ../bin

all : $(PROGRAM) $(OBJECTS) BIN

BIN : $(PROGRAM)
	mkdir -p $(INSTDIR);\
	mv filterBam $(INSTDIR);
	cp $(INSTDIR)/filterBam ../../../bin/filterBam

$(PROGRAM) : $(OBJECTS) 
	$(CXX) $(CFLAGS) $^ -o $@ $(LIBS) 

$(OBJECTS) : %.o:%.cc
	$(CXX) $(CFLAGS) -c $^ -o $@ $(INCLUDES) 


clean: 
	rm -f *~ $(OBJECTS) 
