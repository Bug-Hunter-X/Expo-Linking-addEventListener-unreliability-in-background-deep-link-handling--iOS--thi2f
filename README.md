# Expo Linking.addEventListener unreliability in background deep link handling (iOS)

This repository demonstrates a bug in the Expo `Linking` API, specifically the unreliability of `Linking.addEventListener` when handling deep links while the app is in the background.  The issue appears to be more prevalent on iOS devices.

## Bug Description

The `Linking.addEventListener` method is used to listen for incoming deep links. However, in certain circumstances, particularly when the app is already running in the background, this listener fails to trigger, preventing the app from properly processing the deep link.  This leads to inconsistent and unreliable app behavior.

## Reproduction

Steps to reproduce the bug can be found in the `LinkingBug.js` file.  The solution, demonstrating a workaround, is in `LinkingBugSolution.js`.