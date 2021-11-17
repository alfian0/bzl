MIN_IOS_VERSION = "11.0"

load("@build_bazel_rules_apple//apple:ios.bzl", "ios_application")

ios_application(
    name = "HelloWorldApp",
    bundle_id = "id.privy.HelloWorld",
    families = [
        "iphone",
        "ipad",
    ],
    infoplists = ["Info.plist"],
    minimum_os_version = MIN_IOS_VERSION,
    provisioning_profile = "fe66a10f-bb69-4c6d-b539-347d73ee6b7a.mobileprovision",
    deps = [":HelloWorldAppLibrary"],
)

objc_library(
    name = "HelloWorldAppLibrary",
    srcs = [
        "AppDelegate.m",
        "ViewController.m",
        "main.m"
    ],
    hdrs = [
        "AppDelegate.h",
        "ViewController.h"
    ],
    data = [
        "Base.lproj/LaunchScreen.storyboard",
    ],
    sdk_frameworks = [
        "UIKit",
    ],
    deps = [],
)