# React Native FlatList Rendering Bug

This repository demonstrates a bug where a FlatList in React Native intermittently fails to render data fetched from an API. The issue is not consistent and is difficult to reproduce reliably. 

## Bug Description
The `DataFetch` component fetches data from a public API (`https://jsonplaceholder.typicode.com/todos`). While the data is successfully fetched and available in the component's state, the FlatList sometimes fails to render the items.  This appears to be related to timing or asynchronous operations but the exact cause is elusive.

## How to Reproduce
1. Clone the repository.
2. Run `npm install` to install dependencies.
3. Run `npx react-native run-android` (or `npx react-native run-ios`) to run the app.
4. Observe that the FlatList sometimes renders the data correctly, and sometimes remains blank despite the data being present in the state.

## Solution
The solution involves using a key prop that is unique for each item and wrapping the FlatList renderItem in a function to ensure the keys are consistently available for rendering