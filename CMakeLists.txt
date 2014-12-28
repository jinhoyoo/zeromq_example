cmake_minimum_required (VERSION 2.6)

#For server 
SET(EXECUTABLE server_ex)
project (${EXECUTABLE})
set(SRCS 
	server_ex.c
)
add_executable( ${EXECUTABLE}  ${SRCS})
target_link_libraries( ${EXECUTABLE} libzmq.a -lstdc++ -lpthread -lrt)


#For client
SET(EXECUTABLE client_ex)
project (${EXECUTABLE})
set(SRCS 
	client_ex.c
)
add_executable( ${EXECUTABLE}  ${SRCS})
target_link_libraries( ${EXECUTABLE} libzmq.a -lstdc++ -lpthread -lrt)
