CXX = g++
EXE = $(patsubst %.x, ../%.x, $(wildcard *.x))
LDFLAGS = -L.. -Wl,-rpath=.
LDLIBS = -lgmpxx -lgmp -lnettle -ljsoncpp -lpthread -lhogweed -lstdc++fs -lrt -lmysqlcppconn

all : ../libzeta.so $(EXE)

../libzeta.so : $(wildcard *.o) 
	$(CXX) -shared -o $@ $^ $(LDLIBS)

../%.x : %.x
	$(CXX) $(LDFLAGS) -o $@ $^ -lzeta $(LDLIBS)

