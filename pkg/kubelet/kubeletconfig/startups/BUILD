package(default_visibility = ["//visibility:public"])

licenses(["notice"])

load(
    "@io_bazel_rules_go//go:def.bzl",
    "go_library",
    "go_test",
)

go_library(
    name = "go_default_library",
    srcs = [
        "fstracker.go",
        "startups.go",
    ],
    tags = ["automanaged"],
    deps = [
        "//pkg/apis/componentconfig/validation:go_default_library",
        "//pkg/kubelet/kubeletconfig/util/files:go_default_library",
        "//pkg/kubelet/kubeletconfig/util/filesystem:go_default_library",
        "//pkg/kubelet/kubeletconfig/util/log:go_default_library",
    ],
)

filegroup(
    name = "package-srcs",
    srcs = glob(["**"]),
    tags = ["automanaged"],
    visibility = ["//visibility:private"],
)

filegroup(
    name = "all-srcs",
    srcs = [":package-srcs"],
    tags = ["automanaged"],
)

go_test(
    name = "go_default_test",
    srcs = [
        "fstracker_test.go",
        "startups_test.go",
    ],
    library = ":go_default_library",
    tags = ["automanaged"],
    deps = [
        "//pkg/kubelet/kubeletconfig/util/files:go_default_library",
        "//pkg/kubelet/kubeletconfig/util/filesystem:go_default_library",
        "//pkg/kubelet/kubeletconfig/util/test:go_default_library",
    ],
)
