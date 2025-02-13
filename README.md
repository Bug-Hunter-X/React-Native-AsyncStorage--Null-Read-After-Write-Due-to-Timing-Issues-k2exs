# React Native AsyncStorage Timing Bug

This repository demonstrates a common issue in React Native applications using AsyncStorage.  The problem occurs when reading data from AsyncStorage before the write operation is completely finished. This can result in null values being returned even though the data has been successfully stored.

The `bug.js` file showcases the problematic code, while `bugSolution.js` provides a solution to ensure reliable data retrieval.

## How to Reproduce

1. Clone this repository.
2. Run the application (requires React Native setup).
3. Observe the inconsistent behavior of data retrieval.

## Solution

The solution implemented in `bugSolution.js` involves using promises and `await` to guarantee that the write operation completes before attempting to read the data. This ensures consistent and reliable data access.