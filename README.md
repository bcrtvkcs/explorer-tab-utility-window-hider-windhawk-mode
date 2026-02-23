# Explorer Tab Utility Window Hider - Windhawk Mod
![Screenshot](https://i.imgur.com/bPrN2Xn.png)

This is a Windhawk mod that prevents [w4po](https://github.com/w4po)'s [Explorer Tab Utility](https://github.com/w4po/ExplorerTabUtility) program window from appearing and being visible. The program continues to run in the background, but its window never appears.

## Problem
Explorer Tab Utility normally runs in the background, but sometimes its window becomes visible at computer startup and needs to be manually closed.

## Solution
This Windhawk mod completely blocks the Explorer Tab Utility window. The program continues to run in the background with all its functionality, but its configuration window never appears.

## How It Works
This mod hooks the following Windows API functions:

- **ShowWindow / ShowWindowAsync** - Prevents the window from being shown
- **CreateWindowExW** - Hides the main window immediately after it is created
- **SetWindowPos** - Prevents the window from being made visible via positioning
- **SetForegroundWindow / BringWindowToTop** - Prevents the window from being brought to the front

## Installation
1. Download and install [Windhawk](https://windhawk.net/)
2. Open Windhawk
3. Click "Discover"
4. Search for "Explorer Tab Utility Window Hider"
5. Install the mod
6. You're all set!

## Target Action
This mod is only for Targets the `ExplorerTabUtility.exe` process and does not affect other programs.

## Notes
- The mod hooks multiple Windows API functions to completely block the window.
- The program continues to run in the background and all functions (shortcuts, Explorer tabs, etc.) work.
- You need to temporarily disable the mod to make configuration changes.

## License
All rights reserved. No license specified.
