# gazelle:ignore
load("@io_bazel_rules_go//go:def.bzl", "go_library", "go_test")
load("@org_pubref_rules_protobuf//go:rules.bzl", "GRPC_COMPILE_DEPS")

go_library(
    name = "go_default_library",
    srcs = ["testutil.go"],
    visibility = ["//visibility:public"],
    deps = [
        "//src/proto:go_proto",
    ] + GRPC_COMPILE_DEPS,
)

go_test(
    name = "go_default_test",
    srcs = [
        "bench_test.go",
        "integration_test.go",
    ],
    library = ":go_default_library",
    deps = [
        "//src/proto:go_proto",
        "@in_gopkg_check_v1//:go_default_library",
    ],
)
