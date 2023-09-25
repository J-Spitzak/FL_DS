include ../makeinclude

CPPFILES =\
	main.cxx
ALL =	\
	FL_DS$(EXEEXT) 


all:	$(ALL)

clean:
	$(RM) $(ALL) core main.o

main.o : main.cxx
	$(CXX) -I.. $(ARCHFLAGS) $(CXXFLAGS) -c main.cxx -o main.o

FL_DS$(EXEEXT): main.o
	echo Linking $@...
	$(CXX) -I.. $(ARCHFLAGS) $(CXXFLAGS) $(LDFLAGS) -o $@ main.o -L../../LibDS $(LINKFLTKGL) $(LINKFLTK) $(GLDLIBS) -lLibDS
	$(OSX_ONLY) /Users/1002864/fltk-1.3.8/fltk-config --post $@


