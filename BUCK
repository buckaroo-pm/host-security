xcode_developer_dir = read_config('apple', 'xcode_developer_dir', '/Applications/Xcode.app/Contents/Developer')

genrule(
  name = 'core-services-framework', 
  out = 'CoreServices.framework', 
  cmd = 'cp -r ' + xcode_developer_dir + '/Platforms/MacOSX.platform/Developer/SDKs/MacOSX.sdk/System/Library/Frameworks/CoreServices.framework $OUT', 
)

prebuilt_apple_framework(
  name = 'core-services', 
  framework = ':core-services-framework', 
  preferred_linkage = 'static', 
  visibility = [
    'PUBLIC', 
  ], 
)
