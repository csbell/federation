load("@io_bazel_rules_go//go:def.bzl", "go_library")

go_library(
    name = "go_default_library",
    srcs = ["postal_address.pb.go"],
    importpath = "google.golang.org/genproto/googleapis/type/postaladdress",
    visibility = ["//visibility:public"],
    deps = ["//vendor/github.com/golang/protobuf/proto:go_default_library"],
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
