load("//tensorboard/defs:defs.bzl", "tf_ng_module", "tf_sass_binary", "tf_ts_library")

package(default_visibility = ["//tensorboard:internal"])

licenses(["notice"])

tf_sass_binary(
    name = "style",
    src = "feature_flag_page_component.scss",
    strict_deps = False,
    deps = [
        "//tensorboard/webapp:angular_material_sass_deps",
        "//tensorboard/webapp/theme",
    ],
)

tf_ng_module(
    name = "feature_flag_modal_trigger",
    srcs = [
        "feature_flag_modal_trigger_container.ts",
        "feature_flag_modal_trigger_module.ts",
    ],
    deps = [
        ":views",
        "//tensorboard/webapp:app_state",
        "//tensorboard/webapp/angular:expect_angular_material_dialog",
        "//tensorboard/webapp/feature_flag/actions",
        "//tensorboard/webapp/feature_flag/store",
        "@npm//@angular/common",
        "@npm//@angular/core",
        "@npm//@ngrx/store",
        "@npm//rxjs",
    ],
)

tf_ng_module(
    name = "views",
    srcs = [
        "feature_flag_module.ts",
        "feature_flag_page_component.ts",
        "feature_flag_page_container.ts",
        "types.ts",
    ],
    assets = [
        ":style",
        "feature_flag_page_component.ng.html",
    ],
    deps = [
        "//tensorboard/webapp:app_state",
        "//tensorboard/webapp/angular:expect_angular_material_button",
        "//tensorboard/webapp/angular:expect_angular_material_select",
        "//tensorboard/webapp/feature_flag:types",
        "//tensorboard/webapp/feature_flag/actions",
        "//tensorboard/webapp/feature_flag/store",
        "//tensorboard/webapp/feature_flag/store:feature_flag_metadata",
        "//tensorboard/webapp/feature_flag/store:types",
        "@npm//@angular/common",
        "@npm//@angular/core",
        "@npm//@ngrx/store",
        "@npm//rxjs",
    ],
)

tf_ts_library(
    name = "views_test",
    testonly = True,
    srcs = [
        "feature_flag_modal_trigger_container_test.ts",
        "feature_flag_page_test.ts",
    ],
    deps = [
        ":feature_flag_modal_trigger",
        ":views",
        "//tensorboard/webapp:app_state",
        "//tensorboard/webapp/angular:expect_angular_cdk_testing",
        "//tensorboard/webapp/angular:expect_angular_cdk_testing_testbed",
        "//tensorboard/webapp/angular:expect_angular_core_testing",
        "//tensorboard/webapp/angular:expect_angular_material_dialog",
        "//tensorboard/webapp/angular:expect_angular_material_dialog_testing",
        "//tensorboard/webapp/angular:expect_angular_platform_browser_animations",
        "//tensorboard/webapp/angular:expect_ngrx_store_testing",
        "//tensorboard/webapp/feature_flag:types",
        "//tensorboard/webapp/feature_flag/actions",
        "//tensorboard/webapp/feature_flag/store",
        "//tensorboard/webapp/feature_flag/store:testing",
        "//tensorboard/webapp/testing:utils",
        "@npm//@angular/common",
        "@npm//@angular/core",
        "@npm//@angular/platform-browser",
        "@npm//@ngrx/store",
        "@npm//@types/jasmine",
        "@npm//rxjs",
    ],
)
