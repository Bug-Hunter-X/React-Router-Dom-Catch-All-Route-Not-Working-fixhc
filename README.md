# React Router Dom Catch-All Route Issue

This repository demonstrates a common issue encountered when using the catch-all route (`/*`) in `react-router-dom`.  The problem is that the catch-all route is failing to match any unmatched paths, resulting in unexpected behavior.

## Problem

The `App.js` file contains a basic React Router setup with three routes:

- `/`: Home page
- `/about`: About page
- `/*`: Catch-all route for 404 errors

The expectation is that the catch-all route should match any URL that doesn't match the other routes.  However, in this case, it does not work as intended.

## Solution

The solution is provided in `AppSolution.js`.  The issue was resolved by ensuring the catch-all route (`/*`) is placed last in the `Routes` component. React Router processes routes in the order they are defined. Placing the catch all route at the end guarantees it acts as a true catch all.