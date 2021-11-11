Java Build Tool Bazel with Maven Dependencies Demo
===========================

在Bazel中引用maven dependencies还挺麻烦。

1. 需要在`WORKSPACE`里先下载`rules_jvm_external`，然后再使用它的`maven_install`下载需要的dependency
2. 然后在`BUILD`引用`@maven//:org_apache_commons_commons_lang3`，注意这里label需要转换，把非字母的都转成`_`

有一个问题，不知道在IDEA中，怎么自动将bazel声明的依赖加到`External Libraries`，以方便写代码时引用。

```
brew install bazel
```

```
bazel build :hello
./bazel-bin/hello
```

将会打印出`HELLO`

