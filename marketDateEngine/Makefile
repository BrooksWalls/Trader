# Compiler and flags
CC = gcc
CFLAGS = -Wall -Wextra -std=c11 -g
INCLUDES = -Iinclude

# Directories
SRC_DIR = src
BUILD_DIR = build
INCLUDE_DIR = include

# Source files (automatically find all .c files in src/)
SOURCES = $(wildcard $(SRC_DIR)/*.c)
OBJECTS = $(SOURCES:$(SRC_DIR)/%.c=$(BUILD_DIR)/%.o)

# Target executable name
TARGET = $(BUILD_DIR)/marketdateengine

# Default target
all: $(TARGET)

# Link object files to create executable
$(TARGET): $(OBJECTS)
	@mkdir -p $(BUILD_DIR)
	$(CC) $(OBJECTS) -o $(TARGET)

# Compile source files to object files
$(BUILD_DIR)/%.o: $(SRC_DIR)/%.c
	@mkdir -p $(BUILD_DIR)
	$(CC) $(CFLAGS) $(INCLUDES) -c $< -o $@

# Clean build artifacts
clean:
	rm -rf $(BUILD_DIR)

# Phony targets (not actual files)
.PHONY: all clean

