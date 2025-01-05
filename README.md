# React Native FlatList Unhandled Promise Rejection on API Fetch

This repository demonstrates a bug related to unhandled promise rejections in React Native when using FlatList to display data fetched from an API.  The app intermittently crashes without providing informative error messages.

## Bug Description

The issue involves fetching data from an external API using `fetch` within a `useEffect` hook. The FlatList component then renders the data.  However, under certain (seemingly random) conditions, the promise returned by `fetch` rejects, causing the application to crash silently without logging any useful error information in the console.

## Steps to Reproduce

1. Clone the repository.
2. Run `npm install` to install dependencies.
3. Run the app on an iOS or Android simulator or device.
4. Observe that the app sometimes renders correctly, other times crashing without a clear error.

## Solution

The solution involves comprehensive error handling within the `async` function to catch and handle potential errors during the fetch process, ensuring that any rejections are properly managed and logged to the console, preventing unexpected crashes.  A more robust error handling strategy should be applied in production.
