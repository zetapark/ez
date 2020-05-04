CXX = g++
DIR = $(notdir $(shell pwd))
CPPFLAGS = -I../
CXXFLAGS = -O3 -c -std=c++17 -fmax-errors=1 -fpic
OBJ = $(patsubst %.cc, ../obj/%.$(DIR).o, $(wildcard *.cc))


all : $(OBJ) $(FPIC)

../obj/%.$(DIR).o : %.cc 
	$(CXX) $(CPPFLAGS) $(CXXFLAGS) $< -o $@ 

