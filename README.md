Reproduction for https://github.com/hedronvision/bazel-compile-commands-extractor/issues/163

    D:\hedron_test>bazel run @hedron_compile_commands//:refresh_all
    ERROR: C:/users/marki/_bazel_marki/alqgzwqn/external/hedron_compile_commands/BUILD:7:25: in _transition_py_binary rule @@hedron_compile_commands//:refresh_all:
    Traceback (most recent call last):
        File "C:/users/marki/_bazel_marki/alqgzwqn/external/rules_python/python/config_settings/transition.bzl", line 78, column 13, in _transition_py_impl
                fail("target {} does not have rules_python PyRuntimeInfo or builtin PyRuntimeInfo".format(target))
    Error in fail: target <target @@hedron_compile_commands//:_refresh_all> does not have rules_python PyRuntimeInfo or builtin PyRuntimeInfo
    ERROR: C:/users/marki/_bazel_marki/alqgzwqn/external/hedron_compile_commands/BUILD:7:25: Analysis of target '@@hedron_compile_commands//:refresh_all' failed
    ERROR: Analysis of target '@@hedron_compile_commands//:refresh_all' failed; build aborted
    INFO: Elapsed time: 0.211s, Critical Path: 0.01s
    INFO: 1 process: 1 internal.
    ERROR: Build did NOT complete successfully
    ERROR: Build failed. Not running target
