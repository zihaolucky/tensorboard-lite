# Description:
# TensorBoard plugin for audio

package(default_visibility = ["//tensorboard:internal"])

licenses(["notice"])  # Apache 2.0

exports_files(["LICENSE"])

py_library(
    name = "audio_plugin",
    srcs = ["audio_plugin.py"],
    srcs_version = "PY2AND3",
    visibility = ["//visibility:public"],
    deps = [
        #"//tensorboard:expect_tensorflow_installed",
        "@org_tensorflow//tensorflow/python:platform",
        "@org_tensorflow//tensorflow/python:ops",
        "//tensorboard/backend:http_util",
        "//tensorboard/backend/event_processing:event_accumulator",
        "//tensorboard/plugins:base_plugin",
        "@org_pocoo_werkzeug",
        "@org_pythonhosted_six",
    ],
)

py_test(
    name = "audio_plugin_test",
    size = "small",
    srcs = ["audio_plugin_test.py"],
    srcs_version = "PY2AND3",
    deps = [
        ":audio_plugin",
        "//tensorboard:expect_numpy_installed",
        #"//tensorboard:expect_tensorflow_installed",
        "@org_tensorflow//tensorflow/python:platform",
        "@org_tensorflow//tensorflow/python:summary",
        "@org_tensorflow//tensorflow/python:ops",
        "//tensorboard/backend:application",
        "//tensorboard/backend/event_processing:event_multiplexer",
        "//tensorboard/plugins:base_plugin",
        "@org_pocoo_werkzeug",
        "@org_pythonhosted_six",
    ],
)

py_binary(
    name = "audio_demo",
    srcs = ["audio_demo.py"],
    srcs_version = "PY2AND3",
    deps = [
        #"//tensorboard:expect_tensorflow_installed",
        "@org_tensorflow//tensorflow/python:framework",
        "@org_tensorflow//tensorflow/python:ops",
        "@org_pythonhosted_six",
    ],
)
