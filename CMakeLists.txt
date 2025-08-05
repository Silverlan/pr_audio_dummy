include(${CMAKE_SOURCE_DIR}/cmake/pr_common.cmake)

set(PROJ_NAME pr_audio_dummy)
pr_add_module(${PROJ_NAME} SHARED "modules/audio/dummy/")

pr_add_dependency(${PROJ_NAME} shared TARGET PUBLIC)
pr_add_dependency(${PROJ_NAME} alsoundsystem TARGET PUBLIC)

pr_add_headers(${PROJ_NAME} "include/")
pr_add_sources(${PROJ_NAME} "src/")

pr_finalize(${PROJ_NAME} FOLDER "modules/audio")
