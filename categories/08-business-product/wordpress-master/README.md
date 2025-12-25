# WordPress Master Agent

Elite WordPress architect specializing in full-stack development, performance optimization, and enterprise solutions.

## Overview

The WordPress Master agent is a senior-level WordPress architect with 15+ years of expertise spanning core development, custom solutions, performance engineering, and enterprise deployments. This agent masters PHP/MySQL optimization, JavaScript/React/Vue/Gutenberg development, REST API architecture, and transforms WordPress from a simple CMS into a powerful application framework.

## Key Capabilities

- **Custom Theme Development**: Build modern WordPress themes including block themes, FSE (Full Site Editing), and responsive designs
- **Plugin Development**: Create enterprise-grade plugins with OOP architecture, proper namespacing, and WordPress coding standards
- **Performance Optimization**: Achieve page loads under 1.5s through database optimization, caching strategies, and CDN implementation
- **Security Hardening**: Implement comprehensive security measures to achieve 100/100 security scores
- **Headless WordPress**: Build JAMstack solutions with REST API and GraphQL
- **WooCommerce Mastery**: Develop and optimize e-commerce solutions that scale
- **Multisite Management**: Design and manage WordPress network architectures
- **DevOps & Deployment**: Implement CI/CD pipelines, containerization, and automated deployments

## Performance Targets

- Page load time: < 1.5s
- Database queries: < 50 per page
- PHP memory usage: < 128MB
- Security score: 100/100
- Uptime: > 99.99%
- Core Web Vitals: All green

## Slash Commands

### `/wp-theme`
Create or customize WordPress themes with modern best practices.

**Use cases:**
- Building custom block themes
- Implementing Full Site Editing (FSE)
- Creating child themes
- Converting static HTML to WordPress themes
- Responsive and accessible design implementation

**Example:**
```
/wp-theme Create a custom block theme for a photography portfolio with FSE support
```

### `/wp-plugin`
Develop custom WordPress plugins with professional standards.

**Use cases:**
- Building custom functionality plugins
- Creating admin interfaces
- Implementing REST API endpoints
- Background processing and queue management
- AJAX handling and dynamic features

**Example:**
```
/wp-plugin Build a custom booking system plugin with calendar integration and email notifications
```

### `/wp-security`
Perform comprehensive security audits and implement hardening measures.

**Use cases:**
- Security vulnerability assessment
- File permission configuration
- Database security hardening
- Implementing security headers
- XSS and SQL injection prevention
- Nonce and CSRF protection

**Example:**
```
/wp-security Audit this WordPress installation and implement enterprise-grade security measures
```

### `/wp-optimize`
Analyze and optimize WordPress performance.

**Use cases:**
- Database query optimization
- Implementing object caching (Redis/Memcached)
- Page caching strategies
- Image optimization
- Core Web Vitals improvement
- CDN configuration

**Example:**
```
/wp-optimize Analyze performance bottlenecks and optimize for Core Web Vitals
```

## Technical Expertise

### Core Development
- PHP 8.x optimization and modern features
- MySQL query tuning and database design
- Object caching with Redis/Memcached
- WordPress Core API mastery
- Custom post types and taxonomies
- Advanced meta programming

### Frontend Development
- Gutenberg block development with React
- Block patterns and variations
- Template hierarchy and FSE
- SASS/PostCSS workflows
- JavaScript bundling and optimization
- Accessibility (WCAG 2.1) compliance

### Backend Architecture
- OOP and design patterns (MVC, Repository, Factory)
- Namespace and autoloading
- Hook system mastery
- REST API and GraphQL
- Background processing
- Dependency injection

### Performance Engineering
- Database indexing and optimization
- Query monitoring and profiling
- Multi-tier caching strategies
- CDN implementation
- Critical CSS and lazy loading
- Image optimization pipelines

### Security
- File and database security
- User capability management
- Nonce implementation
- SQL injection prevention
- XSS and CSRF protection
- Security headers and SSL/TLS

### E-commerce
- WooCommerce development
- Payment gateway integration
- Inventory and tax management
- Subscription systems
- Performance scaling for high-traffic stores

### Headless WordPress
- REST API optimization
- GraphQL implementation
- Next.js/Gatsby integration
- JWT authentication
- CORS configuration
- API versioning

## MCP Servers

This agent uses the following MCP servers:

- **filesystem**: Access and manage WordPress files and directories
- **github**: Version control and collaboration
- **context7**: Access WordPress documentation and best practices
- **memory**: Maintain context across development sessions

## Development Workflow

### 1. Architecture Phase
- Audit existing infrastructure
- Establish performance baselines
- Conduct security assessment
- Plan scalability strategies
- Design database schema
- Configure caching layers

### 2. Development Phase
- Write clean, PSR-12 compliant PHP
- Optimize database queries
- Implement caching strategies
- Build custom features
- Create admin interfaces
- Setup automation

### 3. Testing & Optimization
- Performance profiling
- Security testing
- Cross-browser compatibility
- Accessibility validation
- Load testing
- Core Web Vitals measurement

### 4. Deployment
- Environment configuration
- Database migration
- CI/CD pipeline setup
- Monitoring implementation
- Documentation generation

## Integration with Other Agents

The WordPress Master agent collaborates effectively with:

- **seo-specialist**: Technical SEO optimization
- **content-marketer**: CMS features and content workflows
- **security-expert**: Advanced security hardening
- **frontend-developer**: Theme development and customization
- **backend-developer**: API architecture and integration
- **devops-engineer**: Deployment and infrastructure
- **database-admin**: Database optimization and scaling
- **ux-designer**: Admin experience and user interfaces

## Requirements

### Environment
- PHP 8.0 or higher
- WordPress 6.0 or higher
- MySQL 5.7+ or MariaDB 10.2+
- Node.js 18.0+ (for block development)

### Recommended Tools
- Composer for PHP dependency management
- WP-CLI for command-line operations
- Redis or Memcached for object caching
- Varnish for page caching
- Docker for local development
- Git for version control

## Common Use Cases

1. **Custom Theme Development**: Build bespoke themes from scratch or customize existing frameworks
2. **Plugin Development**: Create custom functionality plugins with enterprise-grade architecture
3. **Performance Optimization**: Optimize slow WordPress sites to achieve sub-2-second load times
4. **Security Hardening**: Implement comprehensive security measures for enterprise deployments
5. **WooCommerce Development**: Build and optimize e-commerce solutions
6. **Headless WordPress**: Create modern JAMstack applications
7. **Multisite Networks**: Design and manage WordPress network installations
8. **Migration Projects**: Transfer WordPress sites between hosts or platforms
9. **API Development**: Build custom REST or GraphQL endpoints
10. **Scaling Solutions**: Prepare WordPress sites for high-traffic scenarios

## Best Practices

- Follow WordPress Coding Standards (PSR-12 for PHP)
- Use object caching for database queries
- Implement proper escaping and sanitization
- Utilize WordPress Core functions over custom solutions
- Write comprehensive inline documentation
- Create automated tests for critical functionality
- Use version control for all code changes
- Implement proper error logging and monitoring
- Optimize images and media assets
- Use child themes for customization
- Keep WordPress Core, themes, and plugins updated
- Implement proper backup strategies

## Getting Started

1. Ensure your development environment meets the requirements
2. Configure the MCP servers in your Claude Code setup
3. Use slash commands to invoke specific WordPress workflows
4. Follow the agent's systematic approach to WordPress development
5. Review and test all implementations thoroughly

## Support & Resources

- WordPress Codex: https://codex.wordpress.org/
- WordPress Developer Resources: https://developer.wordpress.org/
- WP-CLI Documentation: https://wp-cli.org/
- WordPress Coding Standards: https://developer.wordpress.org/coding-standards/
- WordPress REST API Handbook: https://developer.wordpress.org/rest-api/

## License

MIT License - See main repository for details.
