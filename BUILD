platform(
    name = "engflow_platform",
    constraint_values = [
        "@platforms//os:linux",
        "@platforms//cpu:x86_64",
        "@bazel_tools//tools/cpp:clang",
    ],
    exec_properties = {
        "container-image": "docker://gcr.io/bazel-public/ubuntu2004-java11@sha256:69a78f121230c6d5cbfe2f4af8ce65481aa3f2acaaaf8e899df335f1ac1b35b5",
        "OSFamily": "Linux",
        "Pool": "linux_x64",
    },
    parents = ["@local_config_platform//:host"],
)

toolchain(
    name = "cc-toolchain",
    exec_compatible_with = [
        "@platforms//os:linux",
        "@platforms//cpu:x86_64",
        "@bazel_tools//tools/cpp:clang",
    ],
    target_compatible_with = [
        "@platforms//os:linux",
        "@platforms//cpu:x86_64",
    ],
    toolchain = "//remote_config/cc:cc-compiler-k8",
    toolchain_type = "@bazel_tools//tools/cpp:toolchain_type",
)