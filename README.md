# cmake

## OpenMP
开启openMP的方法：
### 方法1
target_link_libraries(${target_name} OpenMP::OpenMP_CXX)

### 方法2

find_package(OpenMP REQUIRED)  
if (OPENMP_FOUND)  
&emsp;set (CMAKE_C_FLAGS "${CMAKE_C_FLAGS} ${OpenMP_C_FLAGS}")  
&emsp;set (CMAKE_CXX_FLAGS "${CMAKE_CXX_FLAGS} ${OpenMP_CXX_FLAGS}")  
&emsp;set (CMAKE_EXE_LINKER_FLAGS "${CMAKE_EXE_LINKER_FLAGS} ${OpenMP_EXE_LINKER_FLAGS}")  
endif()  
