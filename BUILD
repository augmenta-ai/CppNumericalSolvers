licenses(["notice"])

exports_files(["LICENSE"])

cc_library(
    name = "cppoptlib",
    srcs = glob([
        "src/*.cpp"
    ]),
    hdrs = glob(
        [
            "include/cppoptlib/*.h",
            "include/cppoptlib/linesearch/*.h",
            "include/cppoptlib/solver/*.h",
            "include/cppoptlib/utils/*.h"
        ]
    ),
    visibility = ["//visibility:public"],
    deps = ["@eigen_archive//:eigen"]
)

load("//:generator.bzl", "build_example", "build_test")

build_example("simple")
build_test("verify")

