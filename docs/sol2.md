# sol2 简介
sol2 是一个现代、轻量、高性能的 C++17/20 头文件库，用于在 C++ 和 Lua 之间进行无缝交互。它是 sol（Simple Object Lua）库的现代版本，提供了更简洁、更安全、更高效的 API。

## 主要特点：
纯头文件库：无需编译，直接包含即可使用
现代 C++ 风格：充分利用 C++17/20 特性
类型安全：编译时类型检查，减少运行时错误
高性能：零开销抽象，接近原生 Lua C API 性能
易用性：简洁直观的 API 设计
异常安全：支持异常处理和错误恢复

# 地址
    https://github.com/ThePhD/sol2

# 安装
    git clone https://github.com/ThePhD/sol2.git
    cd sol2
    mkdir build
    cd build
    cmake ..
    cmake --build . --config Release

# 总结
    sol2 是一个功能强大且易于使用的 C++/Lua 绑定库，特别适合以下场景：

    1. 游戏开发：配置文件、技能系统、AI 脚本
    2. 插件系统：允许用户通过 Lua 扩展应用功能
    3. 配置管理：使用 Lua 作为配置文件格式
    4. 脚本化测试：编写 Lua 测试脚本来验证 C++ 代码
    5. 快速原型开发：用 Lua 快速实现逻辑，后续用 C++ 优化
    
    通过 sol2，开发者可以充分利用 Lua 的灵活性 和 C++ 的性能优势，构建高效、可扩展的应用程序。