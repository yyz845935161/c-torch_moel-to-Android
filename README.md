# c-torch_moel-to-Android
借助wenet将需要使用torch的c++打包为动态链接库.so，且在安卓端使用


torchc++_toAndroid
##0、在Android Studio 中，打开该项目
##1、在文件torchc++_toAndroid\app\src\main\cpp 中写入你自己的.cpp 和.h文件
##2、修改torchc++_toAndroid\app\src\main\cpp\CMakeLists.txt  参照我的
##3、修改 torchc++_toAndroid\app\build.gradle  43行，与CMakeLists一致
##4、参考 torchc++_toAndroid\app\src\main\cpp\wenet.cc  135行代码写cpp文件，将要在安卓上使用的函数暴露出去，注意要和安卓调用端的路径和类名一致
##5、在Android Studio 中，直接点击运行，此时会在torchc++_toAndroid\\app\build\intermediates\stripped_native_libs\debug\out\lib\arm64-v8a，中生成你自己的.so文件



##参考use_so\app\src\main\java\com\example\use_cclib 中调用.so的方法



