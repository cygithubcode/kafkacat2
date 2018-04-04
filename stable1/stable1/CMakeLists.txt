cmake_minimum_required(VERSION 3.9)
project(kafkacat)

set(CMAKE_CXX_STANDARD 11)

message("hi\n")
message(${kafkacat_SOURCE_DIR})
message(${PROJECT_BINARY_DIR})

set(CMAKE_CXX_FLAGS "${CMAKE_CXX_FLAGS} -std=c++11")

add_custom_target(kafkacat COMMAND make -C ${kafkacat_SOURCE_DIR}
        CLION_EXE_DIR=${PROJECT_BINARY_DIR}
        # && cp ${kafkacat_SOURCE_DIR}/make_test ./
        )
#
# add_executable(mykafkacat
#        mklove/modules/configure.cc
#        config.h
#        format.c
#        json.c
#        kafkacat.c
#        kafkacat.h
#        rdport.h
#        tools.c
 #       )
