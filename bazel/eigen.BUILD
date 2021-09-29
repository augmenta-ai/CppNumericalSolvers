# Description:
#   Eigen is a C++ template library for linear algebra: vectors,
#   matrices, and related algorithms.

licenses([
    # Note: Eigen is an MPL2 library that includes GPL v3 and LGPL v2.1+ code.
    #       We've taken special care to not reference any restricted code.
    "reciprocal",  # MPL2
    "notice",  # Portions BSD
])

exports_files(["COPYING.MPL2"])

EIGEN_FILES = [
    "Eigen/**",
    "unsupported/Eigen/**",
]

# List of files picked up by glob but actually part of another target.
EIGEN_EXCLUDE_FILES = [
    "Eigen/src/Core/arch/AVX/PacketMathGoogleTest.cc",
]

EIGEN_MPL2_HEADER_FILES = glob(
    EIGEN_FILES,
    exclude = EIGEN_EXCLUDE_FILES,
)

cc_library(
    name = "eigen",
    hdrs = EIGEN_MPL2_HEADER_FILES,
    includes = ["."],
    visibility = ["//visibility:public"],
)