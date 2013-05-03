cmake_minimum_required(VERSION 2.8.10.20130415)
project(foobar2000-${CMAKE_GENERATOR_TOOLSET})
add_definitions(-DUNICODE=1 -D_UNICODE=1 -D_WIN32_WINNT=0x501 -DBOOST_ALL_NO_LIB=1)
set(USER_COMPONENTS_DIR ${CMAKE_CURRENT_BINARY_DIR}/portable/user-components/)
set_property(GLOBAL PROPERTY USE_FOLDERS ON)

# foreach(flag_var
#         CMAKE_CXX_FLAGS CMAKE_CXX_FLAGS_DEBUG CMAKE_CXX_FLAGS_RELEASE
#         CMAKE_CXX_FLAGS_MINSIZEREL CMAKE_CXX_FLAGS_RELWITHDEBINFO)
#     if(${flag_var} MATCHES "/MD")
#         string(REGEX REPLACE "/MD" "/MT" ${flag_var} "${${flag_var}}")
#     endif()
#     if(${flag_var} MATCHES "/MDd")
#         string(REGEX REPLACE "/MDd" "/MTd" ${flag_var} "${${flag_var}}")
#     endif()
# endforeach(flag_var)

add_subdirectory(wtl)
add_subdirectory(pfc)
add_subdirectory(foobar2000)