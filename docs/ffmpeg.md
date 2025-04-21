# Using FFmpeg with Fusion Studio v20 on Windows, macOS and Linux Usage Tips

A neat feature of Blackmagic Design's Fusion Studio software is that Loader and Saver nodes are able to access obscure video codecs through the use of a user installed FFmpeg shared library (.dll/.dylib/.so).

For a long time, Reactor has hosted an FFmpeg atom package in the "Bin" category that worked with Windows x64 and macOS x64. Until today I didn't know the way to get FFmpeg shared library builds to work on macOS ARM64 or Linux x64.

You start by adding a "FFmpeg:" User PathMap in the Fusion preferences that points to the installation path for the FFmpeg "library" files.

The FFmpeg for Fusion shared library compatibility matrix is as follows:

On Linux/Mac FFmpeg 4, 5 or 6 should work fine. Fusion Studio v20 will be looking for a non-versioned shared library build of libavformat.dylib/so, libavcodec.dylib/so, libavutil.dylib/so, libswscale.dylib/so and libswresample.dylib/so.

On Windows Fusion Studio v20 will be looking for a shared library build of:

FFmpeg 4:

- avformat-58.dll
- avcodec-58.dll
- avutil-56.dll
- swscale-5.dll
- swresample-3.dll

FFmpeg 5:

- avformat-59.dll
- avcodec-59.dll
- avutil-57.dll
- swscale-6.dll
- swresample-4.dll

FFmpeg 6:

- avformat-60.dll
- avcodec-60.dll
- avutil-58.dll
- swscale-7.dll
- swresample-4.dll
