load("@io_bazel_rules_go//go:def.bzl", "go_library", "go_test")

go_library(
    name = "go_default_library",
    srcs = ["image_locality.go"],
    importpath = "k8s.io/kubernetes/pkg/scheduler/framework/plugins/imagelocality",
    visibility = ["//visibility:public"],
    deps = [
        "//pkg/scheduler/framework:go_default_library",
        "//staging/src/k8s.io/api/core/v1:go_default_library",
        "//staging/src/k8s.io/apimachinery/pkg/runtime:go_default_library",
    ],
)

go_test(
    name = "go_default_test",
    srcs = ["image_locality_test.go"],
    embed = [":go_default_library"],
    deps = [
        "//pkg/scheduler/framework:go_default_library",
        "//pkg/scheduler/framework/runtime:go_default_library",
        "//pkg/scheduler/internal/cache:go_default_library",
        "//staging/src/k8s.io/api/core/v1:go_default_library",
        "//staging/src/k8s.io/apimachinery/pkg/apis/meta/v1:go_default_library",
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
    visibility = ["//visibility:public"],
)
