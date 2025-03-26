#### MP 2
###### 1.class声明
在.h文件中已经声明了一个
```h
class Image {
	scale(unsigned w, unsigned h);
}
```
那么 .cpp 文件中实现函数时，就不能再写
```cpp
class Image {
	scale(unsigned w, unsigned h){
		...
	}
}
```
因为相当于重复定义，正确写法是
```cpp
Image::scale(unsigned w, unsigned h){
	...
}
```

###### 2.namespace问题
 **(1)** **命名空间污染**
`using namespace cs225;` 会将 `cs225` 命名空间中的所有符号引入全局作用域，这可能会导致命名冲突。例如，如果 `cs225` 中有一个类或函数与标准库或其他库中的名称相同，编译器将无法区分它们。
 **(2)** **头文件中的 `using namespace`**
在头文件中使用 `using namespace` 是非常不推荐的，因为头文件可能会被多个源文件包含。如果在头文件中使用了 `using namespace`，那么所有包含该头文件的源文件都会受到影响，导致命名空间污染问题。
 **(3)** **类的定义需要明确命名空间**
在你的 `Image.h` 中，`Image` 类继承自 `PNG`，而 `PNG` 是在 `cs225` 命名空间中定义的。如果不在 `Image` 类的定义中明确指定 `cs225::PNG`，编译器将无法正确解析 `PNG` 的类型。
 
 **正确做法
 (1) 在头文件中避免 `using namespace`**
在头文件中，应该避免使用 `using namespace`，而是显式地使用命名空间前缀。例如：
```cpp
#ifndef IMAGE_H
#define IMAGE_H

#include "cs225/PNG.h"

namespace cs225 {
    class Image : public PNG {
    public:
        void lighten(double amount = 0.1);
        void darken(double amount = 0.1);
        void saturate(double amount = 0.1);
        void desaturate(double amount = 0.1);
        void grayscale();
        void rotateColor(double degrees);
        void illinify();
        void scale(double factor);
        void scale(unsigned w, unsigned h);
    };
}

#endif
```
 **(2)** **在源文件中使用 `using namespace`**
在源文件（如 `Image.cpp`）中，可以使用 `using namespace cs225;`，因为它的作用范围仅限于当前文件。例如：

```cpp
#include "Image.h"
#include "cs225/HSLAPixel.h"
#include "cs225/PNG.h"

using namespace cs225;

void Image::lighten(double amount) {
    // 实现代码
}

void Image::darken(double amount) {
    // 实现代码
}

// 其他函数实现...
```
 **(3)** **显式使用命名空间**
如果你不想在源文件中使用 `using namespace cs225;`，也可以显式地使用 `cs225::` 前缀。例如：

```cpp
#include "Image.h"
#include "cs225/HSLAPixel.h"
#include "cs225/PNG.h"

void cs225::Image::lighten(double amount) {
    // 实现代码
}

void cs225::Image::darken(double amount) {
    // 实现代码
}

// 其他函数实现...
```