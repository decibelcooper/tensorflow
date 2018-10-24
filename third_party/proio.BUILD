package(default_visibility = ["//visibility:public"])

licenses(["notice"])

genrule(
    visibility = ["//visibility:public"],
    name = "cp_proto",
    outs = ["proio/proto/proio.proto"],
    srcs = ["proio.proto"],
    cmd = "OUT_DIR=$$(dirname $(OUTS));" +
        "cp $(SRCS) $${OUT_DIR}/",
    #output_to_bindir = 1,
)

genrule(
    visibility = ["//visibility:public"],
    name = "cp_model_proto",
    outs = ["proio/model/eic/eic.proto"],
    srcs = ["model/eic/eic.proto"],
    cmd = "OUT_DIR=$$(dirname $(OUTS));" +
        "cp $(SRCS) $${OUT_DIR}/",
    #output_to_bindir = 1,
)

load(
    "@org_tensorflow//tensorflow/core:platform/default/build_config.bzl",
    "tf_proto_library",
)

tf_proto_library(
    name = "proio.pb",
    srcs = ["proio/proto/proio.proto", "proio/model/eic/eic.proto"],
    visibility = ["//visibility:public"],
    #include = "proio/proto",
)
