load("@bazel_tools//tools/build_defs/repo:git.bzl", "git_repository")
load("@bazel_tools//tools/build_defs/repo:git.bzl", "new_git_repository")
load("@bazel_tools//tools/build_defs/repo:http.bzl", "http_archive")

http_archive(
    name = "rules_proto",
    sha256 = "d8992e6eeec276d49f1d4e63cfa05bbed6d4a26cfe6ca63c972827a0d141ea3b",
    strip_prefix = "rules_proto-cfdc2fa31879c0aebe31ce7702b1a9c8a4be02d2",
    urls = [
        "https://github.com/bazelbuild/rules_proto/archive/cfdc2fa31879c0aebe31ce7702b1a9c8a4be02d2.tar.gz",
    ],
)
load("@rules_proto//proto:repositories.bzl", "rules_proto_dependencies", "rules_proto_toolchains")
rules_proto_dependencies()
rules_proto_toolchains()

git_repository(
    name = "workflow",
    commit = "fafe09a833beab5fc74c709c1d3fe47b63ec9351",
    remote = "https://github.com/sogou/workflow.git")

new_git_repository(
    name = "lz4",
    build_file = "@//third_party:lz4.BUILD",
    commit = "bdc9d3b0c10cbf7e1ff40fc6e27dad5f693a00e7",
    remote = "https://github.com/lz4/lz4.git")

new_git_repository(
    name = "snappy",
    build_file = "@//third_party:snappy.BUILD",
    commit = "78650d126afc55f834d15d018b430985f0c8c87c",
    remote = "https://github.com/google/snappy.git")