load(
    "//tools/bazel:rust.bzl",
    glob = "third_party_glob",
    rust_library = "third_party_rust_library",
)

rust_library(
    name = "bitflags",
    srcs = glob(["vendor/bitflags-1.2.1/src/**"]),
)

rust_library(
    name = "cc",
    srcs = glob(["vendor/cc-1.0.67/src/**"]),
    visibility = ["//visibility:public"],
)

rust_library(
    name = "clap",
    srcs = glob(["vendor/clap-2.33.3/src/**"]),
    edition = "2015",
    visibility = ["//visibility:public"],
    deps = [
        ":bitflags",
        ":textwrap",
        ":unicode-width",
    ],
)

rust_library(
    name = "codespan-reporting",
    srcs = glob(["vendor/codespan-reporting-0.11.1/src/**"]),
    visibility = ["//visibility:public"],
    deps = [
        ":termcolor",
        ":unicode-width",
    ],
)

rust_library(
    name = "lazy_static",
    srcs = glob(["vendor/lazy_static-1.4.0/src/**"]),
    visibility = ["//visibility:public"],
)

rust_library(
    name = "proc-macro2",
    srcs = glob(["vendor/proc-macro2-1.0.26/src/**"]),
    crate_features = [
        "proc-macro",
        "span-locations",
    ],
    rustc_flags = [
        "--cfg=span_locations",
        "--cfg=use_proc_macro",
        "--cfg=wrap_proc_macro",
    ],
    visibility = ["//visibility:public"],
    deps = [":unicode-xid"],
)

rust_library(
    name = "quote",
    srcs = glob(["vendor/quote-1.0.9/src/**"]),
    crate_features = ["proc-macro"],
    visibility = ["//visibility:public"],
    deps = [":proc-macro2"],
)

rust_library(
    name = "scratch",
    srcs = glob(["vendor/scratch-1.0.0/src/**"]),
    rustc_env = {"OUT_DIR": ""},
    visibility = ["//visibility:public"],
)

rust_library(
    name = "syn",
    srcs = glob(["vendor/syn-1.0.68/src/**"]),
    crate_features = [
        "clone-impls",
        "derive",
        "full",
        "parsing",
        "printing",
        "proc-macro",
    ],
    visibility = ["//visibility:public"],
    deps = [
        ":proc-macro2",
        ":quote",
        ":unicode-xid",
    ],
)

rust_library(
    name = "termcolor",
    srcs = glob(["vendor/termcolor-1.1.2/src/**"]),
)

rust_library(
    name = "textwrap",
    srcs = glob(["vendor/textwrap-0.11.0/src/**"]),
    deps = [":unicode-width"],
)

rust_library(
    name = "unicode-width",
    srcs = glob(["vendor/unicode-width-0.1.8/src/**"]),
)

rust_library(
    name = "unicode-xid",
    srcs = glob(["vendor/unicode-xid-0.2.1/src/**"]),
)
