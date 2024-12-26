# React Native FlatList Rendering Issue

This repository demonstrates a common issue encountered when using the FlatList component in React Native: the list fails to render items after a delay introduced by setting the state within the `useEffect` hook. The issue stems from the component potentially unmounting before the state update completes. 

## Bug Report

The initial implementation uses a `setTimeout` function to simulate fetching data from an API. After a 2-second delay, it sets the `items` state, which should trigger a re-render with the fetched data. However, the FlatList remains empty.

## Solution

The solution demonstrates a corrected implementation, preventing the unmounting issue and ensuring data is correctly rendered.