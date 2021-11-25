cmake_minimum_required( VERSION 3.21 FATAL_ERROR )

project(
	HeaderOnlyLibTest
	VERSION     0.1
	DESCRIPTION "Just for testing."
	LANGUAGES   CXX
)

set                        ( HEADERS core.h )
add_library                ( ${PROJECT_NAME} INTERFACE )
target_sources             ( ${PROJECT_NAME} INTERFACE ${CMAKE_CURRENT_SOURCE_DIR}/include/${PROJECT_NAME}/${HEADERS} )
target_compile_features    ( ${PROJECT_NAME} INTERFACE cxx_std_20 )
target_include_directories ( ${PROJECT_NAME} INTERFACE include/ )
