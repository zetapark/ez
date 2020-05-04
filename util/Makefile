CXX = g++
DIR = $(notdir $(shell pwd))
CPPFLAGS = -I../
CXXFLAGS = -std=c++17 -fmax-errors=1
OBJ = $(patsubst %.cc, ../obj/%.$(DIR).o, $(wildcard *.cc))


all : $(OBJ) $(FPIC)

../obj/%.$(DIR).o : %.cc 
	$(CXX) -c $(CPPFLAGS) $(CXXFLAGS) -fpic $< -o $@ 

