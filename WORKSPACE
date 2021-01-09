workspace(name = "lehrbaumm_rustpwn_workspace")

load("@bazel_tools//tools/build_defs/repo:http.bzl", "http_archive")

http_archive(
    name = "io_bazel_rules_rust",
    sha256 = "0e2e633bf0f7f25392ffb477d677c88eb34fe70ffae05e3ad92fdd9f8d6579db",
    strip_prefix = "rules_rust-bc0578798f50d018ca4278ad5610598c400992c9",
    urls = [
        # Master branch as of 2020-12-05
        "https://github.com/bazelbuild/rules_rust/archive/bc0578798f50d018ca4278ad5610598c400992c9.tar.gz",
    ],
)

load("@io_bazel_rules_rust//rust:repositories.bzl", "rust_repositories")

rust_repositories()

load("//pwnd_cli/cargo:crates.bzl", "pwnd_cli_fetch_remote_crates")

pwnd_cli_fetch_remote_crates()

load("//pwnd/cargo:crates.bzl", "pwnd_fetch_remote_crates")

pwnd_fetch_remote_crates()
