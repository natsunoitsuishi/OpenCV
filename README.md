# Build Your OpenCV

<br>

# https://github.com/opencv/opencv/releases/download/4.10.0/opencv-4.10.0-windows.exe

## 使用示例

```cpp
#include <opencv2/opencv.hpp>
#include <iostream>
#include <stdexcept>

int main()
{
    try
    {
        cv::Mat img = cv::imread("test.jpg");
        if (img.empty())
        {
            throw std::runtime_error("Could not read the image");
        }
        cv::imshow("Display window", img);
        cv::waitKey(0);
    }
    catch (const std::exception &e)
    {
        std::cerr << "PUT YOUR IMG INTO THIS PASS ${CMAKE_CURRENT_SOURCE_DIR}/opencv/build/Debug\nOpenCV " << e.what() << std::endl;
    }
    return 0;
}
```

## Build

```cpp
cmake -B build
cd .\build\
cmake --build .
```
