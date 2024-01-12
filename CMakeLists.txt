cmake_minimum_required(VERSION 3.0.0)
project(ffmpeg_project VERSION 0.1.0 LANGUAGES C CXX)

include(CTest)
enable_testing()


set(CPACK_PROJECT_NAME ${PROJECT_NAME})
set(CPACK_PROJECT_VERSION ${PROJECT_VERSION})
include(CPack)

# 测试集
add_subdirectory(test)
# 音频解码成PCM
add_subdirectory(audio_decode)
# 视频添加片尾
add_subdirectory(video_tail)