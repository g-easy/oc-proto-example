http_archive(
    name = "com_github_grpc_grpc",
    urls = ["https://github.com/grpc/grpc/archive/master.tar.gz"],
    strip_prefix = "grpc-master"
)

load("@com_github_grpc_grpc//bazel:grpc_deps.bzl", "grpc_deps")
grpc_deps()

http_archive(
    name = "wrong_name",
    strip_prefix = "opencensus-proto-master/src",  # note: /src
    urls = ["https://github.com/census-instrumentation/opencensus-proto/archive/master.zip"],
)
