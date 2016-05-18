openFrameworks wrapper addon for Ryan C. Gordon's manymouse library.

With this addon you can easily read values from multiple mouse or trackball devices.

Instructions:

1. Add the ofxManyMouse to your project

2. `#include "ofxManyMouse.h"` in ofApp.h

3. let ofApp extend ofxManyMouse like this: 
```cpp
class ofApp : public ofBaseApp, public ofxManyMouse { 
```

4. Add one or more of the following functions to ofApp.h
```cpp
void mouseMoved(int device, int axis, int value);
void mouseMovedAbsolute(int device, int axis, int pos); //new and not tested yet
void mouseScroll(int device, int axis, int value);
void mousePressed(int device, int button);
void mouseReleased(int device, int button);
void mouseDisconnect(int device);
```

5. Implement the function(s) in testApp.cpp
```cpp
void ofApp::mouseMoved(int device, int axis, int value) {
  //do something with the values
}
```

Good luck!


