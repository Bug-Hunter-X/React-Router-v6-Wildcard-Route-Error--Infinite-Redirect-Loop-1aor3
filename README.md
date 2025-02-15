# React Router v6 Wildcard Route Error

This repository demonstrates a common error encountered when using wildcard routes ('/*') in React Router v6.  The issue arises from an infinite redirect loop or unexpected behavior when the wildcard route is defined improperly. The solution demonstrates how to fix this issue by ensuring the wildcard route is the last route defined in the Routes component. 

## Problem

The problem lies in the order of routes.  If a wildcard route is placed before other routes it causes a conflict.  The wildcard route matches everything, which causes the other routes to never be reached. The solution is to ensure the wildcard route is the last defined route. 

## Solution

Moving the wildcard route to be the last route prevents the infinite loop or incorrect routing behavior. The catch-all component will only be rendered if no other routes match.