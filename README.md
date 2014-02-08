This is the Java OpenCV example straight from the [official docs][1], but with
pre-compiled libraries and usage instructions for OSX 10.9 (Mavericks). It may
be useful for others who want to borrow my jar and dylib since they should only
depend on OSX system libraries.

Compile:

    javac -sourcepath . -cp classes:opencv-300.jar com/example/simple/simple.java -d classes

Run:

    java -cp classes:opencv-300.jar com.example.simple.SimpleSample

I compiled OpenCV (172a5d42) starting from the [official docs][1], but they are
heavily geared toward Windows, so I had to improvise to get them to work on OSX
10.9 (Mavericks). The breakthrough for me was pulling up the CMake graphical
configure to turn off all the libraries that were misbehaving (an iterative
process) and to make it a static library build. It's possible that I [could have
used MacPorts][2], but my attempts early on were unsuccessful.

[1]: http://docs.opencv.org/doc/tutorials/introduction/desktop_java/java_dev_intro.html
[2]: http://ladstatt.blogspot.com.br/2013/04/opencv-on-macosx-with-java-support.html
