
add_executable(witest.win7)

target_precompile_headers(witest.win7 PRIVATE ${CMAKE_CURRENT_SOURCE_DIR}/../pch.h)

target_compile_definitions(witest.win7 PRIVATE
    -D_WIN32_WINNT=0x0601
    )

target_sources(witest.win7 PRIVATE
    ${COMMON_SOURCES}
    ${CMAKE_CURRENT_SOURCE_DIR}/../NetworkTests.cpp
    ${CMAKE_CURRENT_SOURCE_DIR}/../RegistryTests.cpp
    ${CMAKE_CURRENT_SOURCE_DIR}/../StlTests.cpp
    ${CMAKE_CURRENT_SOURCE_DIR}/../TokenHelpersTests.cpp
    ${CMAKE_CURRENT_SOURCE_DIR}/../WatcherTests.cpp
    )
