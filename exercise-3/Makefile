CXX := g++
CXXFLAGS := -O3 -std=c++23 -fsanitize=address -S
LDFLAGS := -fsanitize=address

SRC_DIR := src
BUILD_DIR := build

SERVER_SRC := $(SRC_DIR)/tcp_echo_server.cc
CLIENT_SRC := $(SRC_DIR)/tcp_echo_client.cc

SERVER_ASM := $(BUILD_DIR)/server.s
CLIENT_ASM := $(BUILD_DIR)/client.s

all: $(SERVER_ASM) $(CLIENT_ASM)

$(BUILD_DIR):
	mkdir -p $(BUILD_DIR)

$(SERVER_ASM): $(SERVER_SRC) | $(BUILD_DIR)
	$(CXX) $(CXXFLAGS) $< -o $@

$(CLIENT_ASM): $(CLIENT_SRC) | $(BUILD_DIR)
	$(CXX) $(CXXFLAGS) $< -o $@

clean:
	rm -rf $(BUILD_DIR)
