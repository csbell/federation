load("@io_bazel_rules_go//go:def.bzl", "go_binary", "go_library", "go_test")

go_library(
    name = "go_default_library",
    srcs = [
        "blog.go",
        "codewalk.go",
        "dl.go",
        "doc.go",
        "handlers.go",
        "index.go",
        "main.go",
        "play.go",
        "remotesearch.go",
        "x.go",
    ],
    importpath = "golang.org/x/tools/cmd/godoc",
    visibility = ["//visibility:private"],
    deps = [
        "//vendor/golang.org/x/tools/blog:go_default_library",
        "//vendor/golang.org/x/tools/godoc:go_default_library",
        "//vendor/golang.org/x/tools/godoc/analysis:go_default_library",
        "//vendor/golang.org/x/tools/godoc/redirect:go_default_library",
        "//vendor/golang.org/x/tools/godoc/static:go_default_library",
        "//vendor/golang.org/x/tools/godoc/vfs:go_default_library",
        "//vendor/golang.org/x/tools/godoc/vfs/gatefs:go_default_library",
        "//vendor/golang.org/x/tools/godoc/vfs/mapfs:go_default_library",
        "//vendor/golang.org/x/tools/godoc/vfs/zipfs:go_default_library",
        "//vendor/golang.org/x/tools/playground:go_default_library",
    ],
)

go_binary(
    name = "godoc",
    importpath = "golang.org/x/tools/cmd/godoc",
    library = ":go_default_library",
    visibility = ["//visibility:public"],
)

go_test(
    name = "go_default_xtest",
    srcs = [
        "godoc19_test.go",
        "godoc_test.go",
    ],
    importpath = "golang.org/x/tools/cmd/godoc_test",
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
