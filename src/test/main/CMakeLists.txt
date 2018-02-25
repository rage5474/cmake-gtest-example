file(GLOB SRCS *.cpp)

ADD_EXECUTABLE(runtests ${SRCS})

TARGET_LINK_LIBRARIES(runtests
    libgtest
    libgmock
)

add_test(NAME ExampleTest COMMAND runtests)
add_test(NAME AnotherTest COMMAND runtests)
