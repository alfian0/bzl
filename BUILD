MIN_IOS_VERSION = "11.0"

load("@build_bazel_rules_apple//apple:ios.bzl", "ios_application")
load("@build_bazel_rules_swift//swift:swift.bzl", "swift_library")

ios_application(
    name = "HelloWorldApp",
    bundle_id = "id.privy.HelloWorld",
    families = [
        "iphone",
        "ipad",
    ],
    infoplists = ["Info.plist"],
    minimum_os_version = MIN_IOS_VERSION,
    # provisioning_profile = "fe66a10f-bb69-4c6d-b539-347d73ee6b7a.mobileprovision",
    deps = [":HelloWorldAppLibrary"],
)

swift_library(
    name = "HelloWorldAppLibrary",
    srcs = [
        "AppDelegate.swift",
        "ViewController.swift"
    ],
    data = [
        "Base.lproj/LaunchScreen.storyboard",
    ],
)