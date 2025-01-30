# React Native Dimensions API Returns Undefined Width and Height

This repository demonstrates a common issue in React Native where the `Dimensions` API returns `undefined` values for `width` and `height`, even after the component has mounted. This typically occurs because the dimensions are accessed before the layout system has finalized the dimensions.

## Problem
The `Dimensions.get('window')` or `Dimensions.get('screen')` methods might return `undefined` values if called too early in the component's lifecycle, leading to unexpected behavior or crashes.

## Solution
The provided solution shows how to correctly use the `Dimensions` API using the `useEffect` hook and the `Dimensions.addEventListener` to listen for changes to the screen dimensions.  This ensures the dimensions are accessed only after they are available.

## How to reproduce the bug
1. Clone the repository.
2. Run `npm install`.
3. Run `npx react-native run-android` or `npx react-native run-ios`.
4. Observe the initial undefined values for width and height before they update correctly.