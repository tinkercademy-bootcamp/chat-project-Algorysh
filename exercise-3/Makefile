all: build/server.s build/client.s

build/server.s: src/tcp_echo_server.cc | build
	g++ -o build/server.s -S src/tcp_echo_server.cc

build/client.s: src/tcp_echo_client.cc | build
	g++ -o build/client.s -S src/tcp_echo_client.cc

build:
	mkdir -p build
	
clean:
	rm -rf build