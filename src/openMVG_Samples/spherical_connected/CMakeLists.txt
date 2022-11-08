
add_executable(spherical_connected robust_essential_spherical.cpp)
target_link_libraries(spherical_connected
  openMVG_image
  openMVG_multiview
  openMVG_features
  openMVG_matching
  openMVG_system
  openMVG_sfm
  ${STLPLUS_LIBRARY})
target_compile_definitions(spherical_connected
  PRIVATE -DTHIS_SOURCE_DIR="${CMAKE_CURRENT_SOURCE_DIR}")
set_property(TARGET spherical_connected PROPERTY FOLDER OpenMVG/Samples)
