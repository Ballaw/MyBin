CC=gcc
CFLAGS=-Wall -Wextra
INCLUDE_DIR=-I./inc
AR=ar
LIBS=
SOURCES=./src/main.c
ASOBJECTS=$(ASSOURCES:.s=.o)
OBJECTS=$(SOURCES:.c=.o)
TARGET=libNumberTheory.a

all: $(TARGET)

$(TARGET): $(OBJECTS)
	$(AR) rcs $(TARGET) $(OBJECTS)

$(OBJECTS): $(SOURCES)

.c.o:
	$(CC) $(CFLAGS) $(INCLUDE_DIR) -c $< -o $@

clean:
	rm -rf $(OBJECTS) $(TARGET)
