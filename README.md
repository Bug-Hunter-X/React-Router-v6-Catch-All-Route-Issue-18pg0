# React Router v6 Catch-All Route Issue

This repository demonstrates a common issue encountered when using catch-all routes (`/*`) in React Router v6. The catch-all route unintentionally overrides other, more specific routes.

## Problem

The provided `App.js` demonstrates a scenario where a catch-all route (`/*`) prevents other routes from working as expected.  Even if a path matches a more specific route, the catch-all route is triggered.

## Solution

The solution, in `AppSolution.js`, addresses this by rearranging the order of routes.  More specific routes should always be declared *before* the catch-all route in the `Routes` component. This ensures that the more specific routes are checked first.