load("@com_github_grpc_grpc//bazel:cc_grpc_library.bzl", "cc_grpc_library")

# Works:
proto_library(
    name = "foo_proto",
    srcs = ["foo.proto"],
    deps = ["@wrong_name//opencensus/proto/trace/v1:trace_proto"],
)

# Works:
cc_proto_library(
    name = "foo_cc",
    deps = [":foo_proto"],
)

# Doesn't:
cc_grpc_library(
    name = "foo_grpc",
    deps = [":foo_proto"],

    #deps = [":foo_cc"],
    #srcs = ["foo.proto"],
    proto_only = False,
    use_external = True,
    well_known_protos = False,
    #deps = [],
    #"@com_google_protobuf//:timestamp_proto"],
    #deps = ["@wrong_name//opencensus/proto/trace/v1:trace_proto"],
)
