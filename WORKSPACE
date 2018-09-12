http_archive(
    name = "com_github_grpc_grpc",
    urls = ["https://github.com/grpc/grpc/archive/master.tar.gz"],
    strip_prefix = "grpc-master"
)

load("@com_github_grpc_grpc//bazel:grpc_deps.bzl", "grpc_deps")
grpc_deps()

# This used to work:
##http_archive(
##    name = "wrong_name",
##    strip_prefix = "opencensus-proto-master/src",  # note: /src
##    urls = ["https://github.com/census-instrumentation/opencensus-proto/archive/master.zip"],
##)

# This doesn't:
git_repository(
    name = "wrong_name",
    #strip_prefix = "opencensus-proto-master/src",  # Doesn't work.
    #tag = "master",
    commit = "d3b7200dbd14743faa22c6642291d76030833cbd",
    remote = "https://github.com/census-instrumentation/opencensus-proto",
)
