load("//tensorboard/defs:defs.bzl", "tf_ts_library")

package(default_visibility = ["//tensorboard:internal"])

licenses(["notice"])

tf_ts_library(
    name = "actions",
    srcs = [
        "index.ts",
    ],
    deps = [
        "//tensorboard/webapp/metrics:types",
        "//tensorboard/webapp/metrics/data_source",
        "//tensorboard/webapp/metrics/store:types",
        "//tensorboard/webapp/metrics/views/card_renderer:scalar_card_types",
        "//tensorboard/webapp/util:dom",
        "//tensorboard/webapp/widgets/card_fob:types",
        "@npm//@ngrx/store",
    ],
)
