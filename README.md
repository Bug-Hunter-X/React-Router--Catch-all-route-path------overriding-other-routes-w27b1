# React Router Catch-all Route Issue

This repository demonstrates a common issue in React Router where a catch-all route (`path="/*"`) unintentionally overrides other, more specific routes.  The problem occurs because the catch-all route matches any path, including those defined earlier in the `Routes` component.  This effectively renders the other routes unreachable.

## Problem

The provided `App.js` demonstrates the issue.  Even though a route for `/about` is defined, the `/about` path will still be handled by the `NotFound` component, due to how the catch all route is defined.

## Solution

The solution (`AppSolution.js`) shows how to correctly use the catch all route for handling routes that aren't explicitly defined.