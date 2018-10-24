package(default_visibility = ["//visibility:public"])

licenses(["notice"])


cc_library(
    name = "proio",
    srcs = [
        "src/event.cc",
        "src/reader.cc",
        "src/writer.cc",
        ] + [
        "src/event.h",
        "src/reader.h",
        "src/writer.h",
        ] + [
        "@proio_archive//:proio/proto/proio.pb.h",
        ],
    hdrs = [
        "src/event.h",
        "src/reader.h",
        "src/writer.h",
        ],
    deps = [
        "@lz4_archive//:lz4",
        "@proio_archive//:proio.pb_cc",
        ],
)
