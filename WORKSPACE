workspace(name = "com_lightstep_tracer_cpp")

load("@bazel_tools//tools/build_defs/repo:http.bzl", "http_archive")

http_archive(
    name = "io_opentracing_cpp",
    sha256 = "6f4d449e6b411708140d8844aa135f97a8d055bcf4e27334ffa2c1394686451f",
    strip_prefix = "opentracing-cpp-ac50154a7713877f877981c33c3375003b6ebfe1",
    urls = ["https://github.com/opentracing/opentracing-cpp/archive/ac50154a7713877f877981c33c3375003b6ebfe1.tar.gz"],
)

http_archive(
    name = "com_google_protobuf",
    sha256 = "6adf73fd7f90409e479d6ac86529ade2d45f50494c5c10f539226693cb8fe4f7",
    strip_prefix = "protobuf-3.10.1",
    urls = ["https://github.com/google/protobuf/archive/v3.10.1.tar.gz"],
)

http_archive(
    name = "com_google_protobuf_cc",
    sha256 = "6adf73fd7f90409e479d6ac86529ade2d45f50494c5c10f539226693cb8fe4f7",
    strip_prefix = "protobuf-3.10.1",
    urls = ["https://github.com/google/protobuf/archive/v3.10.1.tar.gz"],
)

load("@com_google_protobuf//:protobuf_deps.bzl", "protobuf_deps")

protobuf_deps()

http_archive(
    name = "com_github_grpc_grpc",
    sha256 = "f56ced18740895b943418fa29575a65cc2396ccfa3159fa40d318ef5f59471f9",
    strip_prefix = "grpc-1.23.0",
    urls = ["https://github.com/grpc/grpc/archive/v1.23.0.tar.gz"],
)

load("@com_github_grpc_grpc//bazel:grpc_deps.bzl", "grpc_deps")

grpc_deps()

http_archive(
    name = "io_bazel_rules_go",
    urls = ["https://github.com/bazelbuild/rules_go/releases/download/0.18.5/rules_go-0.18.5.tar.gz"],
    sha256 = "a82a352bffae6bee4e95f68a8d80a70e87f42c4741e6a448bec11998fcc82329",
)

load("@io_bazel_rules_go//go:deps.bzl", "go_rules_dependencies", "go_register_toolchains")
go_rules_dependencies()
go_register_toolchains()

http_archive(
    name = "com_google_googleapis",
    sha256 = "c1969e5b72eab6d9b6cfcff748e45ba57294aeea1d96fd04cd081995de0605c2",
    strip_prefix = "googleapis-be480e391cc88a75cf2a81960ef79c80d5012068",
    urls = ["https://github.com/google/googleapis/archive/be480e391cc88a75cf2a81960ef79c80d5012068.tar.gz"],
)

load("@com_google_googleapis//:repository_rules.bzl", "switched_rules_by_language")

switched_rules_by_language(
    name = "com_google_googleapis_imports",
    cc = True,
    go = True,
    grpc = True,
)
