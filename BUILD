load("@com_github_grpc_grpc//bazel:cc_grpc_library.bzl", "cc_grpc_library")

cc_proto_library(
    name = "trace_cc_proto",
    deps = ["@com_google_googleapis//google/devtools/cloudtrace/v2:trace_proto"],
)

cc_grpc_library(
    name = "trace_cc_grpc",
    srcs = ["@com_google_googleapis//google/devtools/cloudtrace/v2:trace_proto"],
    deps = [":trace_cc_proto"],
    grpc_only = True,
)
