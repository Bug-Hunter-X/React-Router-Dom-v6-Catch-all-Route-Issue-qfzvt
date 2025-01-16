# React Router Dom v6 Catch-all Route Issue

This repository demonstrates a common issue encountered when using catch-all routes ("*" route) in React Router Dom v6.  The catch-all route, intended to handle all non-matched routes, is not functioning correctly.

## Problem

The provided code includes a catch-all route defined as `path="*" element={<NotFound />}`. When navigating to a non-existent path, the `NotFound` component should render. However, in this case, it does not, and instead, the last matched route is rendered. This behavior is inconsistent with expectations.

## Solution

The solution involves placing the catch-all route as the last route within the `Routes` component.  This ensures that it's only reached after all other routes have been checked and failed to match the current URL.

## How to Reproduce

1. Clone this repository.
2. Run `npm install` to install dependencies.
3. Run `npm start` to start the development server.
4. Navigate to a non-existent route (e.g., `/invalid`).  Observe that the `NotFound` component does not render as expected.

## Resolved

The solution provided in `AppSolution.js` addresses the issue by correctly positioning the catch-all route, ensuring that it functions as intended.