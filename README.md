# React Native Dimensions API Inconsistency on Android

This repository demonstrates a common issue encountered when using the `Dimensions` API in React Native on Android devices. The `Dimensions.get('window')` method may return inaccurate screen dimensions under certain circumstances, leading to layout inconsistencies in the application.

## Problem

The `Dimensions` API, while generally reliable, can sometimes provide incorrect width and height values, particularly on Android. This is especially true when dealing with different screen orientations or specific device configurations.  This inconsistency can cause unexpected layout behavior, including elements being clipped, misaligned, or improperly sized.

## Solution

The provided solution uses the `react-native-safe-area-context` library (or similar alternatives) to reliably obtain the screen dimensions, accurately accounting for system UI elements like the status bar and navigation bar. This approach ensures consistent layout across various devices and screen configurations.

## Usage

1. Clone the repository
2. Install dependencies using `npm install` or `yarn install`
3. Run the app using `npx react-native run-android`
4. Observe the difference in reported dimensions between the buggy and corrected implementations.