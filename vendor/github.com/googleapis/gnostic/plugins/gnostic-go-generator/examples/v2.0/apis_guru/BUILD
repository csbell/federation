load("@io_bazel_rules_go//go:def.bzl", "go_binary", "go_library")

go_library(
    name = "go_default_library",
    srcs = ["main.go"],
    importpath = "github.com/googleapis/gnostic/plugins/gnostic-go-generator/examples/v2.0/apis_guru",
    visibility = ["//visibility:private"],
    deps = ["//vendor/github.com/googleapis/gnostic/plugins/gnostic-go-generator/examples/v2.0/apis_guru/apis_guru:go_default_library"],
)

go_binary(
    name = "apis_guru",
    importpath = "github.com/googleapis/gnostic/plugins/gnostic-go-generator/examples/v2.0/apis_guru",
    library = ":go_default_library",
    visibility = ["//visibility:public"],
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
