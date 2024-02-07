workspace(name = "hedron_test")

load("@bazel_tools//tools/build_defs/repo:http.bzl", "http_archive")

# Hedron's Compile Commands Extractor for Bazel
# https://github.com/hedronvision/bazel-compile-commands-extractor
# hedron_compile_commands_commit = "199ca857b05a7a4dbb332e8d229158feb3f82638"
# hedron_compile_commands_commit = "40a51d6164efa2c3dd9e5285962d0062af47c1f1"
hedron_compile_commands_commit = "0e990032f3c5a866e72615cf67e5ce22186dcb97"
http_archive(
    name = "hedron_compile_commands",

    # Replace the commit hash (9335ff4470f3e9238e3aa81aff4b72c528e16c38) in both places (below) with the latest (https://github.com/hedronvision/bazel-compile-commands-extractor/commits/main), rather than using the stale one here.
    # Even better, set up Renovate and let it do the work for you (see "Suggestion: Updates" in the README).
    url = "https://github.com/hedronvision/bazel-compile-commands-extractor/archive/" + hedron_compile_commands_commit + ".tar.gz",
    strip_prefix = "bazel-compile-commands-extractor-" + hedron_compile_commands_commit,
    # When you first run this tool, it'll recommend a sha256 hash to put here with a message like: "DEBUG: Rule 'hedron_compile_commands' indicated that a canonical reproducible form can be obtained by modifying arguments sha256 = ..."
    # sha256 = "6326c883350d86fc111a9c74d8268714144f910907884f4ab4080c17247333a5",
)
load("@hedron_compile_commands//:workspace_setup.bzl", "hedron_compile_commands_setup")
hedron_compile_commands_setup()
load("@hedron_compile_commands//:workspace_setup_transitive.bzl", "hedron_compile_commands_setup_transitive")
hedron_compile_commands_setup_transitive()
load("@hedron_compile_commands//:workspace_setup_transitive_transitive.bzl", "hedron_compile_commands_setup_transitive_transitive")
hedron_compile_commands_setup_transitive_transitive()
load("@hedron_compile_commands//:workspace_setup_transitive_transitive_transitive.bzl", "hedron_compile_commands_setup_transitive_transitive_transitive")
hedron_compile_commands_setup_transitive_transitive_transitive()


http_archive(
    name = "rules_cuda",
    strip_prefix = "rules_cuda-2ccf6bb4da9beda59ebd8fa7e4edfd231d04272e",
    urls = ["https://github.com/bazel-contrib/rules_cuda/archive/2ccf6bb4da9beda59ebd8fa7e4edfd231d04272e.tar.gz"],
    integrity = "sha256-ebl+3qKG3QuTn7atsDL6xOMfeZ1euTgjFgrJ7z7dbOU=",
)

load("@rules_cuda//cuda:repositories.bzl", "register_detected_cuda_toolchains", "rules_cuda_dependencies")
rules_cuda_dependencies()
register_detected_cuda_toolchains()
