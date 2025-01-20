# React useEffect Infinite Loop Bug

This repository demonstrates a common bug in React applications involving the `useEffect` hook.  The bug causes an infinite loop due to improperly updating state within the effect's dependency array.

## Bug Description
The `useEffect` hook is designed to perform side effects after rendering. However, if the state update within the `useEffect` directly depends on the state itself and this effect has no dependencies, a situation of an infinite rendering loop occurs. This can lead to crashes or unresponsive applications.

## Bug Solution
The solution involves using the functional update pattern in `setCount`, ensuring that the state update does not directly depend on the current state value. This breaks the infinite loop, allowing the application to function correctly.