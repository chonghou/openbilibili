load(
    "@io_bazel_rules_go//go:def.bzl",
    "go_library",
    "go_test",
)

go_library(
    name = "go_default_library",
    srcs = [
        "aes.go",
        "auth.go",
        "clean_token.go",
        "contact_bind_log.go",
        "login_log.go",
        "pwd_log.go",
        "service.go",
        "set_token.go",
        "sync_pwd_log.go",
    ],
    importpath = "go-common/app/job/main/passport/service",
    tags = ["automanaged"],
    visibility = ["//visibility:public"],
    deps = [
        "//app/job/main/passport/conf:go_default_library",
        "//app/job/main/passport/dao:go_default_library",
        "//app/job/main/passport/model:go_default_library",
        "//app/service/main/identify-game/model:go_default_library",
        "//app/service/main/identify-game/rpc/client:go_default_library",
        "//library/log:go_default_library",
        "//library/queue/databus:go_default_library",
    ],
)

go_test(
    name = "go_default_test",
    srcs = [
        "aes_test.go",
        "contact_bind_log_test.go",
        "service_test.go",
    ],
    embed = [":go_default_library"],
    rundir = ".",
    tags = ["automanaged"],
    deps = [
        "//app/job/main/passport/conf:go_default_library",
        "//app/job/main/passport/model:go_default_library",
        "//app/service/main/identify-game/model:go_default_library",
        "//library/log:go_default_library",
        "//library/queue/databus:go_default_library",
        "//library/time:go_default_library",
        "//vendor/github.com/smartystreets/goconvey/convey:go_default_library",
    ],
)

filegroup(
    name = "package-srcs",
    srcs = glob(["**"]),
    tags = ["automanaged"],
    visibility = ["//visibility:private"],
)

filegroup(
    name = "all-srcs",
    srcs = [":package-srcs"],
    tags = ["automanaged"],
    visibility = ["//visibility:public"],
)
