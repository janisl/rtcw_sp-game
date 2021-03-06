project(rtcw_sp-game)

cmake_minimum_required(VERSION 2.6)
if(COMMAND cmake_policy)
	cmake_policy(SET CMP0003 NEW)
endif(COMMAND cmake_policy)

option(ENABLE_DEMO "Build demo version")

set(CMAKE_C_FLAGS "${CMAKE_C_FLAGS} -pipe -fsigned-char -fvisibility=hidden")
set(CMAKE_C_FLAGS_DEBUG "${CMAKE_C_FLAGS_DEBUG} -Wall")
set(CMAKE_C_FLAGS_RELEASE "-DNDEBUG -O6 -fomit-frame-pointer -ffast-math -falign-loops=2 -falign-jumps=2 -falign-functions=2 -fno-strict-aliasing -fstrength-reduce")

include(CheckTypeSize)
check_type_size(void*  SIZEOF_VOID_PTR)

if(${SIZEOF_VOID_PTR} MATCHES "8")
	set(ARCH "x86_64")
else()
	set(ARCH "i386")
	set(CMAKE_C_FLAGS_RELEASE "${CMAKE_C_FLAGS_RELEASE} -mcpu=pentiumpro -march=pentium")
endif()
message(STATUS "Using platform suffix ${ARCH}")

if(ENABLE_DEMO)
add_definitions(-DWOLF_SP_DEMO)
endif()

set(LIBRARY_OUTPUT_PATH ${CMAKE_CURRENT_BINARY_DIR})

add_subdirectory(src)
