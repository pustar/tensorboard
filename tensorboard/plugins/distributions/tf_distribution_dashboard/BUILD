package(default_visibility = ["//tensorboard:internal"])

load("//tensorboard/defs:web.bzl", "ts_web_library")

licenses(["notice"])  # Apache 2.0

ts_web_library(
    name = "tf_distribution_dashboard",
    srcs = ["tf-distribution-dashboard.html"],
    path = "/tf-distribution-dashboard",
    deps = [
        "//tensorboard/components/tf_backend",
        "//tensorboard/components/tf_color_scale",
        "//tensorboard/components/tf_dashboard_common",
        "//tensorboard/components/tf_imports:lodash",
        "//tensorboard/components/tf_imports:polymer",
        "//tensorboard/components/tf_runs_selector",
        "//tensorboard/plugins/distributions/vz_distribution_chart",
        "@org_polymer_iron_collapse",
        "@org_polymer_paper_icon_button",
        "@org_polymer_paper_styles",
    ],
)

ts_web_library(
    name = "demo",
    srcs = ["index.html"] + glob(["data/**"]),
    path = "/tf-distribution-dashboard",
    deps = [
        ":tf_distribution_dashboard",
        "//tensorboard/components/tf_imports:d3",
        "//tensorboard/components/tf_imports:webcomponentsjs",
        "@org_polymer_iron_demo_helpers",
        "@org_polymer_paper_styles",
    ],
)

filegroup(
    name = "all_files",
    srcs = glob(["**"]),
    tags = ["notsan"],
)
