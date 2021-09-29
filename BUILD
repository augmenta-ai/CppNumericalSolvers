licenses(["notice"])

exports_files(["LICENSE"])

cc_library(
    name = "cppoptlib",
    srcs = glob([
        "src/*.cpp",
    ]),
    hdrs = glob([
        "include/cppoptlib/*.h",
        "include/cppoptlib/linesearch/*.h",
        "include/cppoptlib/solver/*.h",
        "include/cppoptlib/utils/*.h",
    ]),
    includes = ["include"],
    visibility = ["//visibility:public"],
    deps = [
        "@org_tuxfamily_eigen//:eigen"
    ],
    copts = ["-g"]
)

load("//:generator.bzl", "build_example", "build_test")

build_example("simple")
build_test("verify")

