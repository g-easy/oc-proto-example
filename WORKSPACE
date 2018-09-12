load("@bazel_tools//tools/build_defs/repo:http.bzl", "http_archive")

# Load gRPC and its deps.
http_archive(
    name = "com_github_grpc_grpc",
    urls = ["https://github.com/grpc/grpc/archive/master.tar.gz"],
    strip_prefix = "grpc-master"
)

load("@com_github_grpc_grpc//bazel:grpc_deps.bzl", "grpc_deps")
grpc_deps()

# Google APIs.
http_archive(
    name = "com_google_googleapis",
    strip_prefix = "googleapis-master",
    urls = ["https://github.com/googleapis/googleapis/archive/master.zip"],
)

# Required by googleapis.
http_archive(
    name = "io_grpc_grpc_java",
    urls = ["https://github.com/grpc/grpc-java/archive/master.zip"],
    strip_prefix = "grpc-java-master",
    #tag = "v1.13.1",
)

# Required by googleapis.
http_archive(
    name = "com_google_api_codegen",
    strip_prefix = "gapic-generator-master",
    urls = ["https://github.com/googleapis/gapic-generator/archive/master.zip"],
)

# Required by googleapis.
http_archive(
    name = "io_bazel_rules_go",
    strip_prefix = "rules_go-master",
    urls = ["https://github.com/bazelbuild/rules_go/archive/master.zip"],
)

load("@io_bazel_rules_go//go:deps.bzl", "go_rules_dependencies")
go_rules_dependencies()
