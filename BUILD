cc_library(
    name="dummy",
    hdrs=["dummy.h"],
    srcs=["dummy.cc"],
)

load("@rules_cuda//cuda:defs.bzl", "cuda_library", "cuda_binary")

cuda_binary(
    name = "cuda_example",
    srcs = ["cuda_example.cpp"],
)

