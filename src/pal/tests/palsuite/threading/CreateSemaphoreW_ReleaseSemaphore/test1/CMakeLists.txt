cmake_minimum_required(VERSION 2.8.12.2)

set(CMAKE_INCLUDE_CURRENT_DIR ON)

set(SOURCES
  CreateSemaphore.c
)

add_executable(paltest_createsemaphorew_releasesemaphore_test1
  ${SOURCES}
)

add_dependencies(paltest_createsemaphorew_releasesemaphore_test1 CoreClrPal)

target_link_libraries(paltest_createsemaphorew_releasesemaphore_test1
  pthread
  rt
  m
  CoreClrPal
)
