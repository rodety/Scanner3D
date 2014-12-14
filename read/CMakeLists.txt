cmake_minimum_required(VERSION 2.8)
 
PROJECT(SimplePointsReader)
 
find_package(VTK REQUIRED)
include(${VTK_USE_FILE})
 
add_executable(SimplePointsReader MACOSX_BUNDLE SimplePointsReader)
 
if(VTK_LIBRARIES)
  target_link_libraries(SimplePointsReader ${VTK_LIBRARIES})
else()
  target_link_libraries(SimplePointsReader vtkHybrid vtkWidgets)
endif()


