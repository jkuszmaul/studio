workspace(name = "com_github_google_foxglove")

load("@bazel_tools//tools/build_defs/repo:http.bzl", "http_archive")

http_archive(
    name = "vendored_yarn_3_1_0",
    build_file_content = """exports_files(["vendored_yarn_3_1_0/berry--yarnpkg-cli-3.1.0/packages/yarnpkg-cli/bin/yarn.js"])""",
    urls = ["https://github.com/yarnpkg/berry/archive/refs/tags/@yarnpkg/cli/3.1.0.tar.gz"],
)

http_archive(
    name = "build_bazel_rules_nodejs",
    sha256 = "965ee2492a2b087cf9e0f2ca472aeaf1be2eb650e0cfbddf514b9a7d3ea4b02a",
    urls = ["https://github.com/bazelbuild/rules_nodejs/releases/download/5.2.0/rules_nodejs-5.2.0.tar.gz"],
)

load("@build_bazel_rules_nodejs//:repositories.bzl", "build_bazel_rules_nodejs_dependencies")

build_bazel_rules_nodejs_dependencies()

load("@build_bazel_rules_nodejs//:index.bzl", "node_repositories")

node_repositories(
    node_version = "14.17.0",
)
