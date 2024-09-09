# Hooks in React

React Hooks provide a powerful and flexible way to manage state and side effects in functional components, enhancing code maintainability and reusability.

## Where Do We Need Hooks in React

### 1. Managing State

- React hooks are used to manage state. Hooks like `useState` and `useReducer` enable functional components to maintain internal state.
- This is crucial for scenarios where components need to remember user inputs or manage dynamic data without converting to class components.

### 2. Handling Side Effects

- `useEffect` is used to manage side effects in functional components, like data fetching or manual DOM manipulation.

### 3. Sharing Logic Across Components

- With hooks, we can re-use the stateful logic without altering the component heirarchy.
- Custom hooks can be written to encapsulate shared funcitonality.

### 4. Performance Optimization

- Hooks such as `useMemo` and `useCallback` helps in performance optimization.

### 5. Context Management

- The `useContext` Hook allows components to access context values directly, eliminating the need for prop drilling.
-