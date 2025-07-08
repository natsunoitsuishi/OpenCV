# Link Your Code to OpenCV
<h3 align="center">📦 OpenCV for Windows</h3>

<p align="center">
  <a href="https://github.com/opencv/opencv/releases/download/4.10.0/opencv-4.10.0-windows.exe">
    <img src="https://img.shields.io/badge/Download-OpenCV%204.10.0-blue?style=for-the-badge&logo=windows" alt="Download OpenCV for Windows">
  </a>
</p>
<hr>

## 使用示例

```cpp
#include <opencv2/opencv.hpp>
#include <iostream>
#include <stdexcept>

int main() {
    try {
        cv::Mat img = cv::imread("test.jpg");
        if (img.empty()) {
            throw std::runtime_error("Could not read the image");
        }
        cv::imshow("Display window", img);
        cv::waitKey(0);
    }
    catch (const std::exception &e) {
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
