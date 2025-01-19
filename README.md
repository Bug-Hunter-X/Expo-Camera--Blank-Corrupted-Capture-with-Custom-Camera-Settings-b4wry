# Expo Camera: Blank/Corrupted Capture with Custom Camera Settings

This repository demonstrates a bug in the Expo Camera API where using certain custom camera settings leads to blank or corrupted image/video captures. This appears to be related to compatibility issues between Expo's implementation and some device camera hardware.  The solution involves fallback mechanisms and careful selection of supported camera parameters.

## Reproducing the Bug

1. Clone the repository.
2. `npm install`
3. Run the app on a device or simulator.  Observe that capturing images/videos might fail, resulting in empty or corrupted files.

## Solution

The `bugSolution.js` file offers a solution by adding error handling and fallback mechanisms. It verifies camera capabilities before applying settings and includes error handling during file saving. This increases the resilience of the camera capture process.  It also prioritizes supported camera options to prevent the capture issue.