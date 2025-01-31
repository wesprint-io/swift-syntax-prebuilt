# swift-syntax-prebuilt

This repository is designed to provide pre-built Bazel compatible targets for the [apple/swift-syntax](https://github.com/apple/swift-syntax) repository.

## Usage

Update your `MODULE.bazel` file to override the `swift-syntax` repository with this one.

See the [releases page](https://github.com/wesprint-io/swift-syntax-prebuilt/releases) for available versions.

```starlark
bazel_dep(
    name = "swift-syntax",
    version = "x.x.x",
)

archive_override(
    module_name = "swift-syntax",
    urls = ["https://github.com/wesprint-io/swift-syntax-prebuilt/releases/download/x.x.x/swift-syntax-x.x.x.tar.gz"],
)
```

## Adding `swift-syntax` versions

- Run the [build-publish](https://github.com/wesprint-io/swift-syntax-prebuilt/actions/workflows/build-publish.yml) action.
