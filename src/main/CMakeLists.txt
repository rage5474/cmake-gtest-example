set(MAIN_SRCS
    main.cpp
)

add_executable(hello
    ${MAIN_SRCS}
)

# Specify here the libraries this program depends on
# target_link_libraries(myApp
#     libfoo
#     libbar
# )

install(TARGETS hello DESTINATION bin)
