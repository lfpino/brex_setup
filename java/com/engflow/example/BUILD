package(default_visibility = ["//visibility:public"])

java_library(
    name = "example",
    srcs = glob(["Example.java"]),
)

java_binary(
    name = "example_bin",
    main_class = "com.engflow.example.ExampleBinary",
    srcs = ["ExampleBinary.java"],
    deps = [":example"],
)
