cmake_minimum_required(VERSION 3.0)

project(example-2)

add_executable(roq-samples-example-2
  main.cpp
)

target_include_directories(roq-samples-example-2 PUBLIC
  ${LIBUNWIND_INCLUDE_DIR}
  ${LIBEVENT_INCLUDE_DIR}
  ${GFLAGS_INCLUDE_DIR}
  ${ROQ_API_INCLUDE_DIR}
  ${ROQ_CLIENT_INCLUDE_DIR}
)

target_link_libraries(roq-samples-example-2
  ${CMAKE_THREAD_LIBS_INIT}
  ${LIBUNWIND_LIBS}
  ${LIBEVENT_LIBS}
  ${GFLAGS_LIBS}
  ${ROQ_API_LIBS}
  ${ROQ_CLIENT_LIBS}
)
