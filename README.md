# Expo Constants.manifest Undefined in Background Tasks

This repository demonstrates a bug where `Constants.manifest` is undefined when accessed within background tasks in Expo.  The bug occurs because the app's manifest data might not be fully loaded before the background task begins execution.

## Bug

The `backgroundTaskBug.js` file illustrates the issue. Accessing properties of `Constants.manifest` inside a background task results in undefined values or errors. 

## Solution

The `backgroundTaskSolution.js` file provides a solution.  Instead of directly accessing `Constants.manifest` within the background task, the required manifest data is fetched in the foreground and passed to the background task via an event listener or a shared data store.