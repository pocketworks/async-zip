cmake_minimum_required(VERSION 3.4.1)

add_library(
    async_zip

    # Sets the library as a shared library.
    SHARED

    # Provides a relative path to your source file(s).
    ../ios/Classes/zip.c)

# 16KB page size alignment required for Android 15+ (Google Play requirement)
target_link_options(async_zip PRIVATE "-Wl,-z,max-page-size=16384")

#find_library(
#    log-lib
#    log
#)
#
#target_link_libraries(
#    async_zip
#    ${log-lib}
#)