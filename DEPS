include_rules = [
  "+crypto",
  "+ios/shared/chrome/common",
  "+ios/third_party",
  "+net",
  "+services/network/test",
  "+services/network/public/cpp",
  "+sql",
  "+ui/base",
  "+ui/gfx",

  # Only parts of skia are compiled on iOS, so we explicitly list the
  # files that can be included to avoid bringing in more code.
  "+skia/ext/skia_utils_ios.h",
  "+third_party/skia/include/core/SkBitmap.h",
  "+third_party/skia/include/core/SkColor.h",
  "+third_party/skia/include/core/SkGraphics.h",

  # The subdirectories in ios/chrome/ will manually allow their own include
  # directories in ios/chrome/ so we disallow all of them.
  "-ios/chrome",
  "+ios/chrome/common",
  "+ios/chrome/test",

  "+ios/web/common",
  "+ios/web/public",

  # All code in ios/chrome assumes that web::BrowserState* can be safely
  # casted to ios::ChromeBrowserState*. This mean that no code should use
  # web::TestBrowserState in ios/chrome.
  "-ios/web/public/test/fakes/test_browser_state.h",

  # web::HttpServer is deprecated in favor of net::EmbeddedTestServer.
  # See crbug.com/891834.
  "-ios/web/public/test/http_server",
]
