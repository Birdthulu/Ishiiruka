if(NOT(USE_X11 OR ENABLE_HEADLESS))
  return()
endif()

#[[set(NOGUI_SRCS MainNoGUI.cpp)

add_executable(ishiiruka-nogui ${NOGUI_SRCS})
set_target_properties(ishiiruka-nogui PROPERTIES OUTPUT_NAME ishiiruka-nogui)

target_link_libraries(ishiiruka-nogui PRIVATE
  core
  uicommon
  cpp-optparse
  ${LIBS}
)

if(USE_DISCORD_PRESENCE)
  target_compile_definitions(ishiiruka-nogui PRIVATE -DUSE_DISCORD_PRESENCE)
endif()

set(CPACK_PACKAGE_EXECUTABLES ${CPACK_PACKAGE_EXECUTABLES} ishiiruka-nogui)
install(TARGETS ishiiruka-nogui RUNTIME DESTINATION ${bindir})
]]
