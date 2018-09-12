load("@com_github_grpc_grpc//bazel:cc_grpc_library.bzl", "cc_grpc_library")

proto_library(
    name = "foo_proto",
    srcs = ["foo.proto"],
    deps = ["@wrong_name//opencensus/proto/trace/v1:trace_proto"],
)

cc_proto_library(
    name = "foo_cc",
    deps = [":foo_proto"],
)

# This workaround was mentioned in
# https://github.com/grpc/grpc/issues/14145
proto_library(
    name = "_foo_cc_only",
    srcs = ["foo.proto"],
    deps = ["@wrong_name//opencensus/proto/trace/v1:trace_proto"],
)

cc_grpc_library(
    name = "foo_svc_grpc",
    srcs = ["foo_svc.proto"],
    deps = [":foo_cc"],
    proto_only = False,
    use_external = True,
    well_known_protos = True,  # False -> doesn't work
)
