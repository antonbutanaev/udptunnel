cmake_minimum_required(VERSION 3.7.2)
project(udptunnel)

set(CMAKE_THREAD_PREFER_PTHREAD TRUE)
set(THREADS_PREFER_PTHREAD_FLAG TRUE)
find_package(Threads REQUIRED)

add_executable(udptunnel
	acl.c
	client.c
	list.c
	message.c
	socket.c
	udpclient.c
	udpserver.c
	udptunnel.c
)
set(CMAKE_INSTALL_PREFIX /usr)
install(TARGETS udptunnel DESTINATION bin)
