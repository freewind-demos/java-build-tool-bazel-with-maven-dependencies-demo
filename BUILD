load("@rules_java//java:defs.bzl", "java_binary", "java_library")

java_library(
    name="java-maven-lib",
    srcs = glob(["src/main/java/com/example/*.java"]),
    deps = ["@maven//:org_apache_commons_commons_lang3"],
)

java_binary(
    name = "hello",
    main_class = "com.example.Hello",
    runtime_deps=[":java-maven-lib"]
)