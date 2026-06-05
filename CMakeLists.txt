cmake_minimum_required(VERSION 4.2)
project(meanreversiondev)

set(CMAKE_CXX_STANDARD 20)

add_executable(meanreversiondev main.cpp)


find_package(Boost REQUIRED COMPONENTS system)
find_package(OpenSSL REQUIRED)  # needed for wss (Alpaca)

# -----------------------------
# Link libraries
# -----------------------------
target_link_libraries(meanreversiondev PRIVATE
        Boost::system
        OpenSSL::SSL
        OpenSSL::Crypto
)