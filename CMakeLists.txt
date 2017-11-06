cmake_minimum_required(VERSION 3.10)

find_package(Java REQUIRED)
include(UseJava)

project (HelloWorld)

set(CMAKE_JAVA_TARGET_VERSION 1.0.0)
set(CMAKE_JAVA_COMPILE_FLAGS "-source" "1.9" "-target" "1.9")
set(CMAKE_JAVA_JAR_ENTRY_POINT HelloWorld)

add_jar(HelloWorld 
	SOURCES src/main/java/HelloWorld.java)

