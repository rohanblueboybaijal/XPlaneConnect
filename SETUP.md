### ERRORS

`dlerror:/home/\<username>/X-Plane 11/Resources/plugins/XPlaneConnect/64/lin.xpl: undefined symbol: _ZN3XPC15MessageHandlers21CamCallback_RunwayCamEP20XPLMCameraPosition_tiPv`

This issue is resolved by adding ```CameraCallbacks.cpp``` in the ```CMakeLists.txt``` in both the ```add_library``` commands.

`dlerror:/home/\<username>/X-Plane 11/Resources/plugins/XPlaneConnect/lin.xpl: wrong ELF class: ELFCLASS32`

This is probably an OS compatibility issue with the pre-built binaries.  
Go to ```XPlaneConnect/xpcPlugin```  
```mkdir build```  
```cd build```  
```cmake ..```  
```cmake --build .```  
This will create new .xpl files under a folder named ```XPlaneConnect```. Use that for XPlane.