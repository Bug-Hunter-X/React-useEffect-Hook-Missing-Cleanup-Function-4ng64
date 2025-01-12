# React useEffect Hook Missing Cleanup Function

This example demonstrates a common error in React applications involving the `useEffect` hook: missing a cleanup function to prevent memory leaks and unexpected behavior.

The `useEffect` hook's second argument is an array of dependencies.  If that array is empty, the effect runs only once after the initial render (like `componentDidMount`). If the dependency array contains values, the effect will run each time those values change.

However, without a cleanup function, any side effects set up within the effect will persist even when the component unmounts or the effect is re-run. This leads to unnecessary work and potential memory leaks.