CMAKE_MINIMUM_REQUIRED(VERSION 3.6)

INCLUDE_DIRECTORIES(include)

SET(CMAKE_RUNTIME_OUTPUT_DIRECTORY "${CMAKE_BINARY_DIR}/bin")

SET(CMAKE_CXX_STANDARD 17)

SET(Boost_USE_STATIC_LIBS OFF)
SET(Boost_USE_MULTITHREADED ON)
SET(Boost_USE_STATIC_RUNTIME OFF)

FIND_PACKAGE(Boost 1.69.0 REQUIRED COMPONENTS program_options)

IF(Boost_FOUND)
    INCLUDE_DIRECTORIES(${Boost_INCLUDE_DIRS})
ENDIF()

ADD_SUBDIRECTORY(cat)
ADD_SUBDIRECTORY(seq)
