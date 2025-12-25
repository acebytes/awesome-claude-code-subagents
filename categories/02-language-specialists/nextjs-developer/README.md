# Next.js Developer Agent

Expert Next.js developer specializing in Next.js 14+ with App Router, server components, server actions, and full-stack development. Focused on building blazing-fast, SEO-optimized applications with exceptional user experience.

## Overview

This agent provides comprehensive Next.js development expertise, from architecture planning to production deployment. It excels in modern Next.js patterns, performance optimization, and SEO implementation while maintaining strict TypeScript standards and comprehensive testing coverage.

## Key Features

- **Next.js 14+ App Router**: Master-level expertise in the latest App Router patterns, layouts, and routing strategies
- **Server Components**: Deep knowledge of server component architecture, streaming, and suspense patterns
- **Server Actions**: Secure implementation of form handling, data mutations, and optimistic updates
- **Performance Excellence**: Achieve Core Web Vitals > 90 and SEO scores > 95
- **Full-Stack Development**: Complete database integration, API routes, authentication, and middleware
- **Production Deployment**: Optimized builds, edge runtime, and multi-region deployment strategies
- **TypeScript Strict Mode**: Comprehensive type safety and developer experience
- **Testing Coverage**: Component, integration, E2E, and performance testing

## MCP Servers

This agent uses the following MCP servers:

- **filesystem**: File system operations for reading and writing Next.js project files
- **github**: GitHub integration for repository management and deployments
- **context7**: Access to up-to-date Next.js documentation and best practices
- **memory**: Context retention for project requirements and architectural decisions
- **puppeteer**: Browser automation for testing and performance validation

## Slash Commands

### `/nextjs-page`
Create a new Next.js page with complete App Router structure.

**What it does:**
- Generates page component with proper TypeScript types
- Sets up layout, loading, and error boundary files
- Implements metadata for SEO
- Adds server component patterns
- Includes proper data fetching structure

**Example usage:**
```
/nextjs-page /blog/[slug]
```

### `/nextjs-api`
Generate a new API route with comprehensive error handling and validation.

**What it does:**
- Creates route handler with proper TypeScript types
- Implements request validation and error handling
- Adds authentication middleware integration
- Sets up CORS and security headers
- Includes rate limiting patterns
- Provides comprehensive error responses

**Example usage:**
```
/nextjs-api /api/posts
```

### `/nextjs-deploy`
Optimize and deploy the Next.js application to production.

**What it does:**
- Runs bundle size analysis
- Performs build optimization
- Validates Core Web Vitals scores
- Checks for performance regressions
- Configures environment variables
- Deploys to target platform (Vercel, Docker, etc.)
- Sets up monitoring and alerts

**Example usage:**
```
/nextjs-deploy production
```

### `/nextjs-optimize`
Analyze and optimize Next.js application performance.

**What it does:**
- Analyzes bundle size and composition
- Reviews image optimization opportunities
- Checks font loading strategies
- Evaluates cache strategies
- Measures Core Web Vitals
- Provides actionable optimization recommendations
- Identifies code splitting opportunities
- Reviews edge caching configuration

**Example usage:**
```
/nextjs-optimize
```

## Usage Guide

### Getting Started

1. **Initialize the agent** in your Next.js project directory
2. **Provide project context**: Application type, rendering strategy, data sources, SEO requirements
3. **Choose a workflow**: Architecture planning, implementation, or optimization

### Typical Workflows

#### New Next.js Project
```
1. Initialize project with agent
2. Run architecture planning phase
3. Use /nextjs-page to create route structure
4. Use /nextjs-api for backend endpoints
5. Run /nextjs-optimize for performance tuning
6. Deploy with /nextjs-deploy
```

#### Existing Project Optimization
```
1. Agent analyzes current architecture
2. Run /nextjs-optimize for performance audit
3. Implement recommended optimizations
4. Validate with Core Web Vitals testing
5. Deploy optimizations with /nextjs-deploy
```

#### Adding New Features
```
1. Describe feature requirements
2. Agent plans optimal implementation
3. Use /nextjs-page or /nextjs-api as needed
4. Agent implements with proper patterns
5. Run tests and optimization
```

## Performance Targets

This agent ensures your Next.js application meets or exceeds:

- **Core Web Vitals**: > 90 score
- **SEO Score**: > 95
- **TTFB**: < 200ms
- **FCP**: < 1s
- **LCP**: < 2.5s
- **CLS**: < 0.1
- **FID**: < 100ms

## Architecture Expertise

### App Router Patterns
- Layouts and templates
- Route groups and organization
- Parallel and intercepting routes
- Loading states and error boundaries
- Metadata and SEO optimization

### Rendering Strategies
- Static Site Generation (SSG)
- Server-Side Rendering (SSR)
- Incremental Static Regeneration (ISR)
- Partial Prerendering (PPR)
- Edge runtime optimization
- Client component boundaries

### Data Fetching
- Server component data fetching
- Parallel and sequential patterns
- Cache control and revalidation
- SWR and React Query integration
- Error handling and loading states

### Full-Stack Features
- Database integration (Prisma, Drizzle)
- API route handlers
- Server actions for mutations
- Middleware for authentication
- File upload handling
- WebSocket integration
- Background job processing

## Testing Strategy

- **Component Testing**: React Testing Library for component behavior
- **Integration Tests**: Testing API routes and data flows
- **E2E Testing**: Playwright for user journey validation
- **Performance Testing**: Lighthouse CI and Core Web Vitals monitoring
- **Visual Regression**: Automated screenshot comparison
- **Accessibility Testing**: WCAG compliance validation
- **Load Testing**: Performance under traffic

## Deployment Strategies

### Vercel (Recommended)
- Automatic deployments from Git
- Preview deployments for PRs
- Edge network optimization
- Environment variable management
- Analytics and monitoring

### Self-Hosting
- Docker containerization
- Kubernetes orchestration
- Multi-region deployment
- Load balancing configuration
- CDN integration

### Edge Deployment
- Edge runtime compatibility
- Cloudflare Workers
- AWS Lambda@Edge
- Multi-region edge networks

## Integration with Other Agents

This agent collaborates seamlessly with:

- **react-specialist**: Advanced React patterns and component architecture
- **typescript-pro**: Type safety and TypeScript best practices
- **fullstack-developer**: Full-stack feature implementation
- **database-optimizer**: Database schema and query optimization
- **devops-engineer**: Deployment automation and infrastructure
- **seo-specialist**: Advanced SEO strategies and implementation
- **performance-engineer**: Deep performance optimization
- **security-auditor**: Security audit and vulnerability fixes

## Best Practices Enforced

- TypeScript strict mode enabled
- ESLint and Prettier configured
- Conventional commits for version control
- Semantic versioning for releases
- Comprehensive documentation
- Code review checklist
- Performance budgets maintained
- Security headers configured
- Error boundaries implemented
- Monitoring and alerting active

## Requirements

- Node.js >= 18.0.0
- Next.js >= 14.0.0
- TypeScript (recommended)
- Git for version control

## Environment Setup

Ensure these environment variables are configured:

```bash
# Required for GitHub integration
GITHUB_TOKEN=your_github_token

# Project-specific variables
DATABASE_URL=your_database_url
NEXT_PUBLIC_API_URL=your_api_url
# ... other environment variables
```

## Support and Documentation

For detailed Next.js documentation, the agent uses Context7 MCP server to access the latest:
- Next.js official documentation
- App Router migration guides
- Performance optimization guides
- Deployment best practices
- Security recommendations

## Example Interactions

### Creating a Blog Application
```
User: "Create a blog application with MDX support, dynamic routing, and SEO optimization"

Agent:
1. Analyzes requirements and plans architecture
2. Creates app structure with /nextjs-page
3. Sets up MDX integration and content pipeline
4. Implements dynamic [slug] routing
5. Adds metadata API for SEO
6. Optimizes images and fonts
7. Runs performance validation
8. Provides deployment guide
```

### Optimizing Existing Application
```
User: "My Next.js app is slow, optimize it"

Agent:
1. Runs /nextjs-optimize analysis
2. Identifies bundle size issues
3. Recommends code splitting strategies
4. Optimizes image loading
5. Implements proper caching
6. Converts to server components where applicable
7. Validates Core Web Vitals improvement
8. Provides before/after metrics
```

## License

This agent is part of the Claude Code Agent Marketplace and follows the repository's license terms.

## Contributing

Contributions to improve the Next.js Developer agent are welcome. Please ensure all changes maintain the performance and SEO excellence standards.
