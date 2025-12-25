# Rails Expert Agent

Expert Rails specialist mastering Rails 8.1 with modern conventions. Specializes in convention over configuration, Hotwire/Turbo, Action Cable, and rapid application development with focus on building elegant, maintainable web applications.

## Overview

This agent is a senior Rails expert with deep expertise in:
- Rails 8.1 features including Solid Queue, Solid Cache, and Solid Cable
- Hotwire (Turbo Drive, Turbo Frames, Turbo Streams) for reactive UIs
- Active Record optimization and query performance
- Background job processing with Solid Queue and Sidekiq
- RESTful API development and GraphQL integration
- RSpec testing with comprehensive coverage
- Action Cable for real-time features
- Database design and migrations
- Performance optimization and caching strategies
- Security best practices and authentication

## Installation

### Prerequisites

- Node.js >= 18.0.0
- PostgreSQL database
- GitHub Personal Access Token (for GitHub integration)
- Redis (optional, for Action Cable and caching)

### Environment Setup

Set the following environment variables:

```bash
export GITHUB_TOKEN="your_github_personal_access_token"
export POSTGRES_URL="postgresql://user:password@localhost:5432/database"
```

### MCP Servers

This agent uses the following MCP servers:

1. **filesystem** - File system operations for code generation
2. **github** - GitHub repository integration for version control
3. **context7** - Rails documentation and context retrieval
4. **memory** - Persistent memory and context management
5. **postgres** - Direct database operations and schema inspection

## Slash Commands

### /rails-model

Generate a Rails model with associations, validations, tests, and migrations.

**Example Usage:**
```
/rails-model User with email, name, and has_many posts
```

This command will:
- Create model file with proper ActiveRecord setup
- Add associations (belongs_to, has_many, has_one, etc.)
- Include validations (presence, uniqueness, format, etc.)
- Generate database migration with appropriate columns
- Create comprehensive RSpec model specs
- Add FactoryBot factory definitions
- Include database indexes for performance

**Advanced Usage:**
```
/rails-model Product with name, price:decimal, category:references, description:text, and validates presence of name, uniqueness of sku
```

### /rails-controller

Create a Rails controller with RESTful actions, strong parameters, and tests.

**Example Usage:**
```
/rails-controller Posts with index, show, create, update, destroy
```

This command will:
- Generate controller with specified actions
- Add proper strong parameters (params.require/permit)
- Include error handling and status codes
- Create comprehensive request specs
- Add route definitions to config/routes.rb
- Follow Rails RESTful conventions
- Include pagination for index actions

**Advanced Usage:**
```
/rails-controller Api::V1::Users with create, update, destroy, and custom action send_verification_email
```

### /rails-test

Generate comprehensive RSpec tests for existing Rails code.

**Example Usage:**
```
/rails-test Order model with payment processing and status transitions
```

This command will:
- Create appropriate spec type (model, request, system, etc.)
- Cover all validations and associations
- Test business logic and edge cases
- Include factory definitions with FactoryBot
- Test scopes, callbacks, and custom methods
- Ensure high test coverage (95%+)
- Follow RSpec best practices
- Add shared examples where appropriate

**Advanced Usage:**
```
/rails-test PaymentController with Stripe integration, webhooks, and refund handling
```

### /rails-migrate

Create and manage database migrations.

**Example Usage:**
```
/rails-migrate add_stripe_customer_id_to_users
```

This command will:
- Generate migration file with proper timestamp
- Include both up and down methods
- Add appropriate indexes for foreign keys
- Consider data types and constraints
- Ensure migration is reversible
- Follow Rails migration best practices
- Add comments for complex migrations

**Advanced Usage:**
```
/rails-migrate create_orders_table with user:references, total:decimal, status:string, shipped_at:datetime, and index on user_id and status
```

## Capabilities

### Rails 8.1 Features
- Solid Queue for background jobs
- Solid Cache for high-performance caching
- Solid Cable for WebSocket connections
- Import maps for JavaScript management
- Turbo and Stimulus integration
- Active Storage for file uploads
- Action Text for rich text content
- Action Mailbox for incoming emails

### Application Architecture
- MVC pattern implementation
- RESTful resource design
- Service objects for business logic
- Form objects for complex forms
- Query objects for complex queries
- Decorator pattern with Draper
- Concerns for shared behavior
- Policy objects with Pundit

### Hotwire Integration
- Turbo Drive for seamless page navigation
- Turbo Frames for partial page updates
- Turbo Streams for real-time updates
- Stimulus controllers for JavaScript sprinkles
- Broadcasting with Action Cable
- Progressive enhancement approach

### Performance Optimization
- N+1 query elimination with includes/joins
- Fragment caching and Russian doll caching
- Database query optimization
- Eager loading strategies
- Background job offloading
- CDN integration for assets
- Database indexing strategies
- Memory profiling and optimization

### Testing Excellence
- Model specs with RSpec
- Request specs for API testing
- System specs with Capybara
- FactoryBot for test data
- Shared examples and contexts
- VCR for HTTP interaction recording
- Test coverage with SimpleCov
- Performance testing with Benchmark

### API Development
- RESTful API design
- JSON API serialization with Jbuilder
- API versioning strategies
- Authentication with JWT or OAuth
- Rate limiting with Rack::Attack
- API documentation with Swagger
- GraphQL API with graphql-ruby
- CORS configuration

## Quality Standards

The Rails Expert maintains high quality standards:

- **Test Coverage**: Target > 95%
- **Response Time**: Average < 50ms
- **Performance Score**: Target > 90
- **Ruby Version**: 3.2+
- **Rails Version**: 8.1+
- **Security**: Regular audits with Brakeman
- **Code Quality**: RuboCop compliance
- **Database**: Optimized queries, proper indexing

## Example Use Cases

### 1. Build an E-commerce Platform
```
Create a full-featured e-commerce application with product catalog, shopping cart, checkout with Stripe, order management, and admin dashboard using Rails 8.1 and Hotwire
```

### 2. RESTful API Development
```
Design and implement a RESTful API for a mobile app with user authentication, JWT tokens, rate limiting, versioning, and comprehensive documentation
```

### 3. Real-time Chat Application
```
/rails-model Message with user:references, room:references, body:text, read_at:datetime
Build a real-time chat feature using Action Cable, Turbo Streams, and Redis for presence tracking
```

### 4. Background Job Processing
```
Implement email newsletter system with Solid Queue for job processing, ActiveJob for email delivery, and retry strategies for failed jobs
```

### 5. Database Optimization
```
/rails-test analyze and optimize the Product.search query that's causing N+1 issues
Optimize complex queries, add appropriate indexes, and implement caching strategies
```

### 6. Legacy Rails Migration
```
Migrate legacy Rails 5.2 application to Rails 8.1, upgrading dependencies, replacing asset pipeline with import maps, and modernizing with Hotwire
```

## Development Workflow

### 1. Architecture Planning
- Review project requirements and constraints
- Design database schema and relationships
- Plan RESTful routes and resources
- Define service layer boundaries
- Establish caching strategy
- Set up testing approach
- Plan deployment pipeline

### 2. Implementation
- Generate models with associations
- Create controllers with RESTful actions
- Build views with Hotwire components
- Implement service objects
- Add background jobs
- Write comprehensive tests
- Configure caching and optimization

### 3. Quality Assurance
- Run RSpec test suite
- Check test coverage with SimpleCov
- Profile performance with Rack Mini Profiler
- Audit security with Brakeman
- Review code with RuboCop
- Test real-time features
- Verify deployment readiness

## Integration with Other Agents

The Rails Expert works seamlessly with:

- **ruby-specialist** - Ruby optimization and advanced patterns
- **fullstack-developer** - Full-stack Rails integration
- **postgres-pro** - Database design and optimization
- **frontend-developer** - Hotwire and Stimulus integration
- **devops-engineer** - Deployment and infrastructure
- **performance-engineer** - Performance optimization strategies
- **api-designer** - API design and documentation
- **security-auditor** - Security best practices and auditing

## Advanced Features

### Hotwire Excellence
- Turbo Drive for SPA-like navigation
- Turbo Frames for independent page sections
- Turbo Streams for real-time updates
- Stimulus for JavaScript behavior
- Progressive enhancement strategy
- Optimistic UI updates
- Broadcasting patterns

### Active Record Mastery
- Complex associations (polymorphic, STI, delegated types)
- Custom scopes and query methods
- Callbacks and lifecycle hooks
- Validations and custom validators
- Database views with Scenic
- Full-text search with pg_search
- Soft deletes with paranoia

### Background Jobs
- Solid Queue for built-in job processing
- Sidekiq for high-performance jobs
- Job prioritization and scheduling
- Retry strategies and error handling
- Job monitoring and metrics
- Batch processing patterns
- Scheduled jobs with cron

### Security Best Practices
- Authentication with Devise
- Authorization with Pundit
- CSRF protection
- SQL injection prevention
- XSS prevention
- Secure credential management
- Regular security audits
- Rate limiting and throttling

## Best Practices

1. **Convention Over Configuration**
   - Follow Rails conventions and idioms
   - Use standard directory structure
   - Leverage Rails generators
   - Follow naming conventions

2. **Testing**
   - Write tests first (TDD)
   - Test behavior, not implementation
   - Use factories, not fixtures
   - Maintain high coverage (95%+)

3. **Performance**
   - Prevent N+1 queries
   - Use appropriate caching
   - Add database indexes
   - Profile before optimizing

4. **Code Quality**
   - Keep controllers skinny
   - Extract business logic to services
   - Use concerns judiciously
   - Follow Ruby style guide

5. **Security**
   - Use strong parameters
   - Implement authentication/authorization
   - Regular dependency updates
   - Security audit with Brakeman

## Troubleshooting

### Common Issues

**N+1 queries:**
```
Use includes, eager_load, or preload to optimize queries
/rails-test analyze query performance for Products index
```

**Slow tests:**
```
Profile with RSpec --profile flag, reduce database hits, use build_stubbed
```

**Performance problems:**
```
Profile with Rack Mini Profiler, check database queries, implement caching
```

**Migration issues:**
```
/rails-migrate rollback and fix, ensure reversibility, test in development
```

## Support

For issues, improvements, or questions about this agent:
- Check existing documentation in CLAUDE.md
- Review example use cases above
- Consult with related specialist agents
- Reference official Rails Guides
- Check Rails 8.1 release notes

## Resources

- [Rails Guides](https://guides.rubyonrails.org/)
- [Rails API Documentation](https://api.rubyonrails.org/)
- [Hotwire Documentation](https://hotwired.dev/)
- [RSpec Rails Documentation](https://rspec.info/documentation/3.12/rspec-rails/)
- [Ruby Style Guide](https://rubystyle.guide/)

## License

Part of the Claude Agent Marketplace - Language Specialists category.
