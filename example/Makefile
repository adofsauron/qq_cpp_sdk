
RM = /bin/rm -f
CP = /bin/cp

CC = g++

CPPFLAGS =  -g -rdynamic -Wall -D_REENTRANT  

LIBS =  $(LIB_OPENAPI) $(LIB_JSON) $(LIB_OAUTH) $(LIB_CURL) $(LIB_OPENSSL)  -lrt  -ldl
INCL =  $(INC_OPENAPI) $(INC_JSON)  $(INC_OPENSSL) $(INC_OAUTH) $(INC_CURL)   -I./include

SOURCES      := $(wildcard *.cpp)
TARGETS      := $(patsubst %.cpp, %, $(SOURCES))

all: $(TARGETS)

%: %.cpp Makefile
	$(CC)  -o $@  $(CPPFLAGS) $< $(INCL) $(LIBS)

clean:
	$(RM) $(DEPENDS) $(TARGETS)
	$(RM) *.o














