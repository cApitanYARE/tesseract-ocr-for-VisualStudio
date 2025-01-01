# tesseract-ocr-for-VisualStudio

# tesseract-ocr-for-VisualStudio-MSVC

path = "D:\dev_tesseract\"
path is the play where you install "tesseract.rar"

first of all in Visual Studio you need open "Properties" after open "C/C++" choose General and in "Additional Include Directories" input this:
1) path\tesseract\tesseract\leptonica\src;
2) path\tesseract\tesseract\include;
3) path\tesseract\tesseract\build_tesseract\include;
4) path\tesseract\tesseract\build_leptonica\src\Debug;
5) path\tesseract\tesseract\build_tesseract\Debug;
6) path\tesseract\tesseract\build_leptonica\src;

second you need to open "Linker" choose "General" and in "Additional Include Directories" input this:
1) path\tesseract\tesseract\build_tesseract\Debug;
2) path\tesseract\tesseract\build_leptonica\src\Debug;
3) path\tesseract\tesseract\leptonica\dependencies\build\build_openjpeg\bin\Debug;
4) path\tesseract\tesseract\leptonica\dependencies\build\build_libjpeg-turbo\Debug;
5) path\tesseract\tesseract\leptonica\dependencies\build\build_zlib\Debug;
6) path\tesseract\tesseract\leptonica\dependencies\build\build_libpng\Debug;
7) path\tesseract\tesseract\leptonica\dependencies\build\build_giflib\Debug;
9) path\tesseract\tesseract\leptonica\dependencies\build\build_libwebp\Debug;
10) path\tesseract\tesseract\leptonica\dependencies\build\build_libtiff\libtiff\Debug

at last in "LInker" open "Input" and in "Additional Include Directories" input this:
1) tesseract55d.lib;
2) leptonica-1.85.1d.lib;
3) openjp2.lib;
4) jpeg.lib;
5) jpeg-static.lib;
6) zlibd.lib;
7) libpng_ad.lib;
8) giflibd.lib;
9) libwebp.lib;
10) libsharpyuv.lib;
11) tiffd.lib;

simple way:
tesseract55d.lib;leptonica-1.85.1d.lib;openjp2.lib;jpeg.lib;jpeg-static.lib;zlibd.lib;libpng_ad.lib;giflibd.lib;libwebp.lib;libsharpyuv.lib;tiffd.lib;

but maybe when you try to launch project you can get error, then you need open "System" on your PC after this "additional settings" then "variables" after open and you will see
"Path" add this and project will be lounch witout errors

1)path\tesseract\tesseract\build_tesseract\bin\Debug
2) path\tesseract\tesseract\leptonica\dependencies\build\build_openjpeg\bin\Debug
3) path\tesseract\tesseract\leptonica\dependencies\build\build_libjpeg-turbo\Debug
4) path\tesseract\tesseract\leptonica\dependencies\build\build_zlib\Debug
5) path\tesseract\tesseract\leptonica\dependencies\build\build_libtiff\libtiff\Debug

and one more this "Pix* image = pixRead("D:/dev_tesseract/tesseract/icon.png")" is where located your image for work

ENJOI