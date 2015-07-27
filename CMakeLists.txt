add_library(libsel4benchmark STATIC
    src/sel4_benchmark.c
)

target_compile_definitions(libsel4benchmark
    PUBLIC HAVE_SEL4_BENCHMARK
)

target_include_directories(libsel4benchmark SYSTEM
    PUBLIC "include"
)

target_link_libraries(libsel4benchmark
    libsel4
    libsel4printf)
