# Uncomment this line to define a global platform for your project
platform :ios, '9.0'
# Uncomment this line if you're using Swift
use_frameworks!

target ‘RKitBase’ do
  pod 'sdl-rkx', :path => ‘0.1’
  pod 'ResearchKit', '~> 1.3'
end


#allows ResearchKit to build,
#per https://github.com/ResearchKit/ResearchKit/issues/679
#and https://github.com/cornelltech/sdl-rkx/issues/1
#Remove once resolved
post_install do |installer|
  installer.pods_project.targets.each do |target|
    target.build_configurations.each do |config|
      config.build_settings['GCC_NO_COMMON_BLOCKS'] = 'NO'
    end
  end
end
