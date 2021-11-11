Java Build Tool Bazel Demo
===========================

Bazel是一种支持多语言混合编译的构建工具。

这里是最简单的Java例子，没有用到第三方库，只是打印出一句话。

注意：
1. `WORKSPACE`文件是用来表示当前项目是一个可能包含多个package的workspace
2. `BUILD`文件表示所在目录是一个package，可以在里面使用一种类似python的语言[starlark](https://docs.bazel.build/versions/4.2.1/skylark/language.html)进行配置。
   每个包含`BUILD`文件的目录都是一个package，内部可以使用不同语言实现功能

```
brew install bazel
```

```
bazel build //:ProjectRunner
./bazel-bin/ProjectRunner
```

将会打印出`Hello`

