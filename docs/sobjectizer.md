## SObjectizer

    这是一个在相当小巧的 C++ 框架中实现 Actor、发布/订阅和 CSP 模型的框架。其性能、质量和稳定性已在多年的生产环境中得到验证

    Objectizer 是为数不多的跨平台开源 C++ “Actor 框架”之一。但 SObjectizer 不仅支持 Actor 模型，还支持发布/订阅模型和类似 CSP 的通道。SObjectizer 的目标是显著简化 C++ 中并发和多线程应用程序的开发。

    SObjectizer 允许将并发应用程序创建为一组代理对象，这些代理对象通过异步消息相互交互。它负责消息分发，并为消息处理提供工作上下文。此外，它还允许通过提供各种即用型分发器来调整这些功能。

# 下载地址
    https://github.com/Stiffstream/sobjectizer

# 安装
    git clone https://github.com/Stiffstream/sobjectizer.git

    cd sobjectizer

    mkdir build

    cd build

    cmake ..

    cmake --build . --config Release

# 参考示例代码
    #include <so_5/all.hpp>

    class hello_actor final : public so_5::agent_t {
    public:
    using so_5::agent_t::agent_t;

    void so_evt_start() override {
        std::cout << "Hello, World!" << std::endl;
        // Finish work of example.
        so_deregister_agent_coop_normally();
    }
    };

    int main() {
    // Launch SObjectizer.
    so_5::launch([](so_5::environment_t & env) {
            // Add a hello_actor instance in a new cooperation.
            env.register_agent_as_coop( env.make_agent<hello_actor>() );
        });

    return 0;
    }
