project(superpiexl_feature)

find_package(OpenCV REQUIRED)

include_directories( include )

add_executable(superpixel_feature j2seg.cpp)

#target_link_libraries(superpixel_feature  /home/xduser/LiHuan/SuperPixel_Feature/lib/libjpeg.a /home/xduser/LiHuan/SuperPixel_Feature/lib/libSLIC.a /home/xduser/LiHuan/SuperPixel_Feature/lib/libopencv_lbp.a)
# link to libjpeg.a cause to imread() failed

target_link_libraries(superpixel_feature /home/xduser/LiHuan/SuperPixel_Feature/lib/libSLIC.a /home/xduser/LiHuan/SuperPixel_Feature/lib/libopencv_lbp.a)

target_link_libraries(superpixel_feature ${OpenCV_LIBS} )





