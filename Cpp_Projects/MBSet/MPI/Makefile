# Makefile for OPENGL examples

# CFLAGS   = -gstabs -I. -I$(HOME)/Software/OpenGLLinks
# CXXFLAGS = -gstabs -I. -I$(HOME)/Software/OpenGLLinks
#LDFLAGS  = -g -framework Carbon -framework GLUT -framework OpenGL
LDFLAGS  = -g -O3 -lglut -lGLU -lGL 
CCFLAGS = -g -O3
CXXFLAGS = -g -O3 -Wall
CFLAGS = -

#CXX = /Developer/usr/bin/g++-4.0
#CC  = /Developer/usr/bin/gcc-4.0
CXX = /usr/bin/mpic++
# CC  = /usr/bin/gcc

MBSet:	MBSet.o complex.o
	$(CXX) -o MBSet MBSet.o complex.o $(LDFLAGS)

MBSet.o:	MBSet.cc

complex.o:	complex.cc

clean:
	@rm -f MBSet MBSet.o complex.o

%o:	%.cc
	@echo Compiling $*
	$(CXX) $(CXXFLAGS) -c $*.cc

%o:	%.c
	@echo Compiling $*
	$(CC) $(CFLAGS) -c $*.c

%:	%.o
	@echo Linking $*
	$(CXX) -o $* $*.o $(LDFLAGS)

%:	%.cc
	@echo Compiling/Linking $*
	$(CXX) $(CXXFLAGS) -o $* $*.cc $(LDFLAGS)

%:	%.c
	@echo Compiling/Linking $*
	$(CC) $(CCFLAGS) -o $* $*.c $(LDFLAGS)



