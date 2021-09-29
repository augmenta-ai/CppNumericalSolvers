load("@bazel_tools//tools/build_defs/repo:http.bzl", "http_archive")
load("@bazel_tools//tools/build_defs/repo:git.bzl", "new_git_repository")

# load the eigen library
http_archive(
    name = "org_tuxfamily_eigen",
    build_file = "@//bazel:eigen.BUILD",
    sha256 = "d56fbad95abf993f8af608484729e3d87ef611dd85b3380a8bad1d5cbc373a57",
    strip_prefix = "eigen-3.3.7",
    urls = [
        "https://agmt-public.s3.us-east-2.amazonaws.com/install/eigen-3.3.7.tar.gz",
    ],
)

http_archive(
    name = "gtest",
    url = "https://github.com/google/googletest/archive/release-1.7.0.zip",
    sha256 = "b58cb7547a28b2c718d1e38aee18a3659c9e3ff52440297e965f5edffe34b6d0",
    build_file = "@//bazel:gtest.BUILD",
    strip_prefix = "googletest-release-1.7.0",
)
