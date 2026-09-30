# livox_sdk_vendor
ROS 2 vendor package for https://github.com/Livox-SDK/Livox-SDK2 (built with `ament_vendor`).

Consumers add `<depend>livox_sdk_vendor</depend>` to their `package.xml`; the SDK's `lib/` and `include/` are then on `CMAKE_PREFIX_PATH`, so `find_library(... liblivox_lidar_sdk_shared.so)` and `find_path(... livox_lidar_api.h)` resolve without extra CMake.
