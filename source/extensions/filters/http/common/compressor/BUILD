load(
    "//bazel:envoy_build_system.bzl",
    "envoy_cc_library",
    "envoy_extension_package",
)

licenses(["notice"])  # Apache 2

envoy_extension_package()

# TODO(rojkov): move this library to source/extensions/filters/http/compressor/.
envoy_cc_library(
    name = "compressor_lib",
    srcs = ["compressor.cc"],
    hdrs = ["compressor.h"],
    deps = [
        "//envoy/compression/compressor:compressor_interface",
        "//envoy/stats:stats_macros",
        "//envoy/stream_info:filter_state_interface",
        "//source/common/buffer:buffer_lib",
        "//source/common/http:header_map_lib",
        "//source/common/http:utility_lib",
        "//source/common/protobuf",
        "//source/common/runtime:runtime_lib",
        "//source/extensions/filters/http/common:pass_through_filter_lib",
        "@envoy_api//envoy/extensions/filters/http/compressor/v3:pkg_cc_proto",
    ],
)
