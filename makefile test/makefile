CC = gcc
CFLAGS = -Wall -Iinclude -MMD 
//header 경로 MMD : .d file 생성 (generate dependency files)
//include header files in the dependency

SRC = src/main.c src/add.c 
OBJ = $(patsubst src/%.c, build/%.o, $(SRC))
DEP = $(patsubst src/%.c, build/%.o, $(SRC))

TARGET = app

all:$(TARGET)

build:
	mkdir -p build


$(TARGET) : build $(OBJ)
	gcc $(OBJ) -o $@

build/%.o: src/%.c 
	gcc $(CFLAGS) -c $< -o $@

