# TypeScript Pro Agent

Expert TypeScript developer specializing in advanced type system usage, full-stack development, and build optimization. Masters type-safe patterns for both frontend and backend with emphasis on developer experience and runtime safety.

## Overview

The TypeScript Pro agent is your expert companion for advanced TypeScript development. It specializes in leveraging TypeScript 5.0+ features to build type-safe, performant applications across the full stack. Whether you're building a React frontend, a Node.js backend, or managing a complex monorepo, this agent ensures maximum type safety and optimal developer experience.

## Key Capabilities

- **Advanced Type System**: Master conditional types, mapped types, template literals, and type-level programming
- **Full-Stack Type Safety**: Implement end-to-end type safety with tRPC, GraphQL, and shared type definitions
- **Build Optimization**: Configure tsconfig, project references, and optimize compilation performance
- **Framework Expertise**: Deep knowledge of React, Vue, Angular, Next.js, NestJS, and more
- **Type-Driven Development**: Design type-first APIs and leverage the compiler for correctness
- **Migration Support**: Guide JavaScript to TypeScript migrations and modernize existing codebases
- **Quality Assurance**: Achieve 100% type coverage with strict mode and comprehensive testing

## Slash Commands

### `/ts-analyze`
Perform comprehensive TypeScript code analysis including:
- Type coverage assessment
- Compiler diagnostics and error analysis
- Build performance metrics
- Bundle size analysis
- Generic usage patterns
- Type complexity metrics

**Example usage:**
```
/ts-analyze
```

### `/ts-type-check`
Run strict type checking across the project:
- Identify type safety gaps
- Review strict mode compliance
- Check for implicit any usage
- Validate generic constraints
- Provide improvement recommendations

**Example usage:**
```
/ts-type-check
```

### `/ts-refactor`
Refactor code to improve type safety:
- Apply advanced type patterns (discriminated unions, branded types)
- Optimize type inference
- Replace any types with proper types
- Implement type guards and predicates
- Extract reusable type utilities

**Example usage:**
```
/ts-refactor src/api/handlers.ts
```

### `/ts-migrate`
Guide migration and modernization:
- JavaScript to TypeScript conversion
- Upgrade to modern TypeScript features
- Migrate to strict mode
- Implement type-safe patterns
- Preserve runtime behavior

**Example usage:**
```
/ts-migrate --from-js src/legacy/
```

## MCP Servers

This agent uses the following MCP servers:

- **filesystem**: Read and write project files, manage TypeScript configurations
- **github**: Access repository code, review PRs, analyze type definitions
- **context7**: Fetch up-to-date TypeScript and framework documentation
- **memory**: Store project context, type patterns, and configuration preferences

## Getting Started

### Prerequisites

- TypeScript 5.0 or higher
- Node.js 18 or higher
- A TypeScript project or willingness to start one

### Basic Usage

1. **Project Setup**: The agent will analyze your existing tsconfig.json and package.json
2. **Type Analysis**: Use `/ts-analyze` to understand your current type coverage
3. **Implementation**: Work with the agent to implement type-safe features
4. **Quality Check**: Use `/ts-type-check` to ensure strict type compliance

### Example Workflows

#### Starting a New TypeScript Project
```
I need to set up a new TypeScript project with React and Node.js backend.
I want full-stack type safety with tRPC.
```

#### Improving Type Safety
```
/ts-analyze
/ts-type-check

Please help me achieve 100% type coverage by removing all any types
and implementing proper type guards.
```

#### Migrating from JavaScript
```
/ts-migrate src/

Guide me through migrating this JavaScript codebase to TypeScript
with strict mode enabled.
```

#### Optimizing Build Performance
```
My TypeScript compilation is slow. Please analyze and optimize:
- tsconfig.json settings
- Project references
- Module resolution
- Build times
```

## Best Practices

The TypeScript Pro agent follows these principles:

1. **Strict Mode Always**: Enable all strict compiler flags for maximum safety
2. **No Implicit Any**: Every value should have an explicit type
3. **Type-First Design**: Design types before implementation
4. **100% Coverage**: Aim for complete type coverage on public APIs
5. **Performance Matters**: Optimize both compile-time and runtime performance
6. **Developer Experience**: Prioritize clear error messages and IDE support
7. **Documentation**: Maintain comprehensive type documentation

## Integration with Other Agents

TypeScript Pro works well with:

- **frontend-developer**: Share component types and props
- **backend-developer**: Provide Node.js and API types
- **react-developer**: Advanced React TypeScript patterns
- **api-designer**: Type-safe API contracts
- **fullstack-developer**: End-to-end type safety
- **javascript-developer**: Migration guidance

## Advanced Features

### Type-Level Programming
Build complex type transformations and validations at compile time.

### Full-Stack Type Safety
Implement end-to-end type safety from database to UI with tRPC, Prisma, and type-safe forms.

### Monorepo Support
Configure TypeScript project references for optimal build performance in monorepos.

### Library Authoring
Create type-safe libraries with excellent developer experience and backward compatibility.

### Code Generation
Generate types from OpenAPI specs, GraphQL schemas, and database schemas.

## Troubleshooting

### Slow Compilation
The agent can analyze and optimize:
- tsconfig.json settings
- Project references setup
- Module resolution strategy
- Incremental compilation
- Type complexity

### Type Errors
Get help with:
- Complex generic constraints
- Type inference issues
- Union and intersection types
- Conditional type problems
- Module augmentation

### Migration Issues
Guidance on:
- Gradual JavaScript to TypeScript conversion
- Third-party type definitions
- Ambient declarations
- Breaking changes in TypeScript versions

## Resources

- TypeScript Documentation: https://www.typescriptlang.org/docs/
- TypeScript Deep Dive: https://basarat.gitbook.io/typescript/
- Type Challenges: https://github.com/type-challenges/type-challenges
- tRPC: https://trpc.io/

## Support

For issues, questions, or contributions, visit the [Claude Code Agent Marketplace](https://github.com/anthropics/claude-code-agent-marketplace).
