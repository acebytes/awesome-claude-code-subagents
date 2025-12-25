# React Specialist Agent

Expert React specialist mastering React 18+ with modern patterns and ecosystem. Specializes in performance optimization, advanced hooks, server components, and production-ready architectures with focus on creating scalable, maintainable applications.

## Overview

This agent is a senior React specialist with deep expertise in:
- React 18+ features and concurrent rendering
- Advanced component patterns and custom hooks
- Performance optimization and profiling
- State management solutions (Redux, Zustand, Jotai, Recoil)
- Server-side rendering with Next.js and Remix
- Comprehensive testing strategies
- TypeScript integration and type safety
- Accessibility compliance
- Bundle optimization and code splitting

## Installation

### Prerequisites

- Node.js >= 18.0.0
- GitHub Personal Access Token (for GitHub integration)

### Environment Setup

Set the following environment variable:

```bash
export GITHUB_TOKEN="your_github_personal_access_token"
```

### MCP Servers

This agent uses the following MCP servers:

1. **filesystem** - File system operations
2. **github** - GitHub repository integration
3. **context7** - Documentation and context retrieval
4. **memory** - Persistent memory and context management
5. **puppeteer** - Browser automation for testing and debugging

## Slash Commands

### /react-component

Create a new React component with TypeScript, following best practices for composition, accessibility, and testing.

**Example Usage:**
```
/react-component UserProfile with avatar, bio, and social links
```

This command will:
- Generate a TypeScript React component
- Include proper prop types and interfaces
- Add accessibility attributes
- Create a companion test file
- Follow atomic design principles

### /react-hooks

Design and implement custom React hooks with proper dependencies, memoization, and TypeScript typing.

**Example Usage:**
```
/react-hooks useDebounce for search input with configurable delay
```

This command will:
- Create a custom hook with TypeScript types
- Implement proper dependency management
- Add memoization where appropriate
- Include usage examples and documentation
- Generate hook tests

### /react-test

Generate comprehensive tests for React components using React Testing Library, covering user interactions and edge cases.

**Example Usage:**
```
/react-test LoginForm component with validation and error handling
```

This command will:
- Create test suite using React Testing Library
- Cover user interactions and workflows
- Test edge cases and error states
- Include accessibility tests
- Achieve high code coverage

### /react-optimize

Analyze and optimize React component performance using profiling, memoization, code splitting, and bundle analysis.

**Example Usage:**
```
/react-optimize Dashboard component with heavy data rendering
```

This command will:
- Profile component rendering performance
- Identify unnecessary re-renders
- Apply React.memo, useMemo, useCallback
- Implement code splitting strategies
- Analyze and reduce bundle size
- Provide performance metrics

## Capabilities

### Component Development
- React 18+ functional components
- TypeScript strict mode
- Compound components
- Render props and HOCs
- Error boundaries
- Suspense boundaries

### Performance Optimization
- React.memo for component memoization
- useMemo for expensive calculations
- useCallback for function optimization
- Code splitting with lazy loading
- Virtual scrolling for large lists
- Concurrent rendering features

### State Management
- Redux Toolkit for complex state
- Zustand for lightweight state
- Jotai atoms for atomic state
- Recoil for advanced patterns
- Context API for shared state
- React Query for server state

### Server-Side Rendering
- Next.js App Router and Pages Router
- Remix loaders and actions
- Server components
- Streaming SSR
- Static site generation
- Incremental static regeneration

### Testing
- React Testing Library for component tests
- Jest for unit and integration tests
- Cypress for E2E testing
- Hook testing with renderHook
- Performance testing
- Accessibility testing

### Ecosystem Integration
- React Query/TanStack Query for data fetching
- React Hook Form for forms
- Framer Motion for animations
- Tailwind CSS for styling
- Material-UI and Ant Design
- TypeScript for type safety

## Quality Standards

The React Specialist maintains high quality standards:

- **Performance Score**: Target > 95 (Lighthouse)
- **Test Coverage**: Target > 90%
- **Component Reusability**: Target > 80%
- **TypeScript**: Strict mode enabled
- **Accessibility**: WCAG 2.1 AA compliance
- **Bundle Size**: Optimized and analyzed
- **Best Practices**: ESLint, Prettier, conventional commits

## Example Use Cases

### 1. Build a Complex React Application
```
Create a dashboard application with real-time data, charts, and user management using Next.js 14 with server components
```

### 2. Performance Optimization
```
/react-optimize ProductList component - currently rendering 1000 items with performance issues
```

### 3. State Management Implementation
```
Set up Redux Toolkit for e-commerce app with cart, user, and product slices
```

### 4. Component Library Creation
```
/react-component Button component with variants (primary, secondary, danger), sizes, and loading states
```

### 5. Testing Suite Setup
```
/react-test complete test coverage for CheckoutForm including payment validation and error handling
```

### 6. Migration Project
```
Migrate legacy React class components to modern hooks, implementing concurrent features and improving performance
```

## Development Workflow

### 1. Architecture Planning
- Review project requirements and constraints
- Design component hierarchy
- Plan state management approach
- Define performance targets
- Establish testing strategy

### 2. Implementation
- Create reusable components
- Implement state management
- Add routing and navigation
- Optimize performance
- Write comprehensive tests
- Ensure accessibility compliance

### 3. Quality Assurance
- Run performance profiling
- Verify test coverage
- Check accessibility
- Analyze bundle size
- Review code quality
- Document components

## Integration with Other Agents

The React Specialist works seamlessly with:

- **frontend-developer** - UI patterns and design systems
- **fullstack-developer** - Full-stack React integration
- **typescript-pro** - Type safety and advanced TypeScript
- **javascript-pro** - Modern JavaScript patterns
- **performance-engineer** - Performance optimization strategies
- **qa-expert** - Testing strategies and quality assurance
- **accessibility-specialist** - Accessibility compliance
- **devops-engineer** - Deployment and CI/CD pipelines

## Advanced Features

### Concurrent Rendering
- useTransition for non-urgent updates
- useDeferredValue for delayed rendering
- Suspense for data fetching
- Automatic batching for state updates

### Server Components
- React Server Components (RSC)
- Streaming SSR with Suspense
- Progressive hydration
- Selective hydration

### Modern Patterns
- Compound components for flexible APIs
- Custom hooks for reusable logic
- Context optimization with useMemo
- Portal patterns for modals and tooltips
- Ref forwarding for DOM access

## Best Practices

1. **Component Design**
   - Keep components small and focused
   - Use composition over inheritance
   - Implement proper prop types
   - Follow atomic design principles

2. **Performance**
   - Avoid unnecessary re-renders
   - Use code splitting strategically
   - Implement virtual scrolling for long lists
   - Optimize bundle size

3. **State Management**
   - Keep state as local as possible
   - Use appropriate state solution for use case
   - Avoid prop drilling with Context
   - Separate server and client state

4. **Testing**
   - Test user behavior, not implementation
   - Achieve high coverage
   - Include accessibility tests
   - Mock external dependencies

5. **Type Safety**
   - Enable TypeScript strict mode
   - Define proper interfaces
   - Avoid 'any' type
   - Use type inference

## Troubleshooting

### Common Issues

**Performance problems:**
```
/react-optimize <component-name>
```

**Test failures:**
```
/react-test <component-name> --verbose
```

**Type errors:**
Consult with typescript-pro agent for complex type issues

**Bundle size:**
Run bundle analysis and implement code splitting

## Support

For issues, improvements, or questions about this agent:
- Check existing documentation in CLAUDE.md
- Review example use cases above
- Consult with related specialist agents
- Reference official React documentation

## License

Part of the Claude Agent Marketplace - Language Specialists category.
