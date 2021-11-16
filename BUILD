MIN_IOS_VERSION = "13.0"

load("@build_bazel_rules_apple//apple:ios.bzl", "ios_application")

ios_application(
    name = "HelloWorldApp",
    bundle_id = "com.google.mediapipe.HelloWorld",
    families = [
        "iphone",
        "ipad",
    ],
    infoplists = ["Info.plist"],
    minimum_os_version = MIN_IOS_VERSION,
    # provisioning_profile = "//mediapipe/examples/ios:developer_provisioning_profile",
    deps = [":HelloWorldAppLibrary"],
)

objc_library(
    name = "HelloWorldAppLibrary",
    srcs = [
        "AppDelegate.m",
        "ViewController.m",
        "main.m",
        "SceneDelegate.m"
    ],
    hdrs = [
        "AppDelegate.h",
        "ViewController.h",
        "SceneDelegate.h"
    ],
    data = [
        "Base.lproj/LaunchScreen.storyboard",
        "Base.lproj/Main.storyboard",
    ],
    sdk_frameworks = [
        "UIKit",
    ],
    deps = [],
)