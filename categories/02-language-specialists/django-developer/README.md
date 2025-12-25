# Django Developer Agent

Expert Django developer mastering Django 4+ with modern Python practices. Specializes in scalable web applications, REST API development, async views, and enterprise patterns with focus on rapid development and security best practices.

## Overview

The Django Developer agent is a specialized AI assistant for building robust, scalable Django applications. It combines deep knowledge of Django 4+, Python 3.11+, and modern web development practices with automated tooling for rapid application development.

## Key Features

### Core Expertise
- **Django 4+ Development**: Full mastery of Django's MVT architecture, batteries-included philosophy
- **ORM Optimization**: Query optimization, select_related/prefetch_related, custom managers
- **REST API Development**: Django REST Framework, serializers, viewsets, authentication
- **Async Capabilities**: Async views, ASGI deployment, WebSocket support with Channels
- **Security First**: CSRF protection, XSS prevention, SQL injection defense, security headers
- **Performance Focus**: Query optimization, caching strategies, async processing, CDN integration

### Advanced Capabilities
- Multi-tenancy architecture
- GraphQL API development
- Full-text search with Elasticsearch
- GeoDjango for location-based features
- Custom middleware and management commands
- Admin interface customization
- Internationalization (i18n/l10n)

## Slash Commands

### `/django-model`
Create a new Django model with proper field types, validators, and methods.

```bash
# Basic usage
/django-model Product

# Specify app name
/django-model User auth

# Create with relationships
/django-model BlogPost blog
```

**What it does**:
1. Analyzes existing models for consistency
2. Creates model with appropriate fields and relationships
3. Adds Meta class with ordering and indexes
4. Implements `__str__` method
5. Adds custom managers if needed
6. Includes model methods for business logic
7. Generates migration file
8. Updates admin.py registration

### `/django-view`
Create Django views (function-based or class-based) with proper error handling.

```bash
# API view
/django-view api ProductListView

# Function-based view
/django-view fbv login_view

# Async view
/django-view async dashboard_view
```

**What it does**:
1. Determines view type (FBV, CBV, or async)
2. Implements view with proper decorators/mixins
3. Adds authentication and permission checks
4. Includes form/serializer handling
5. Adds context data processing
6. Implements error handling
7. Creates URL pattern
8. Writes view tests

### `/django-test`
Generate comprehensive tests for Django models, views, or APIs.

```bash
# Test a model
/django-test model User

# Test a view
/django-test view ProductListView

# Test an API endpoint
/django-test api product-list
```

**What it does**:
1. Analyzes component to be tested
2. Creates test class with proper setup
3. Generates factory/fixture data
4. Writes unit tests for all methods
5. Adds integration tests if applicable
6. Includes edge case testing
7. Adds performance tests where relevant
8. Verifies test coverage > 90%

### `/django-migrate`
Create and apply Django migrations with conflict resolution.

```bash
# Check and apply all migrations
/django-migrate

# Migrate specific app
/django-migrate auth

# Check migrations without applying
/django-migrate products --check
```

**What it does**:
1. Reviews pending model changes
2. Checks for migration conflicts
3. Generates migration files
4. Reviews migration SQL
5. Applies migrations to database
6. Handles migration errors/conflicts
7. Updates migration history
8. Verifies database state

## MCP Servers

### Filesystem
Provides file system access for reading/writing Django project files.
```bash
npx -y @modelcontextprotocol/server-filesystem ${PWD}
```

### GitHub
Enables repository operations, PR management, and code review.
```bash
# Requires GITHUB_TOKEN environment variable
npx -y @modelcontextprotocol/server-github
```

### Context7
Provides access to Django and Python documentation.
```bash
npx -y @upstash/context7-mcp
```

### Memory
Maintains conversation context and project knowledge.
```bash
npx -y @modelcontextprotocol/server-memory
```

### Postgres
Direct PostgreSQL database access for schema inspection and queries.
```bash
# Requires POSTGRES_URL environment variable
npx -y @modelcontextprotocol/server-postgres
```

## Setup

### Prerequisites
- Python 3.11 or higher
- Django 4.0 or higher
- Node.js (for MCP servers)
- PostgreSQL (recommended)

### Environment Variables

```bash
# Optional: GitHub integration
export GITHUB_TOKEN="your_github_personal_access_token"

# Optional: PostgreSQL database
export POSTGRES_URL="postgresql://user:password@localhost:5432/django_db"
```

### Installation

1. Clone or download the agent configuration:
```bash
cd /path/to/your/django/project
```

2. The agent will use MCP servers automatically when invoked.

3. Ensure your Django project has the recommended dependencies:
```bash
pip install django>=4.0 \
    djangorestframework>=3.14 \
    pytest-django>=4.5 \
    celery>=5.3 \
    redis>=4.5 \
    psycopg2-binary>=2.9
```

## Usage Examples

### Creating a Complete Django App

```markdown
Create a blog application with:
- Post model with title, content, author, published_date
- Category model with many-to-many relationship to Post
- REST API endpoints for CRUD operations
- Admin interface with filters and search
- Tests with >90% coverage
```

The agent will:
1. Design the model schema
2. Create models with proper relationships
3. Generate migrations
4. Build REST API with DRF
5. Customize admin interface
6. Write comprehensive tests
7. Optimize queries with select_related

### Optimizing Database Queries

```markdown
Analyze and optimize the Product listing API. It's currently slow with N+1 queries.
```

The agent will:
1. Analyze current query patterns
2. Identify N+1 query issues
3. Apply select_related/prefetch_related
4. Add database indexes
5. Implement caching
6. Benchmark improvements
7. Update tests

### Implementing Authentication

```markdown
Add JWT authentication to the API with refresh tokens and email verification.
```

The agent will:
1. Configure Django REST Framework JWT
2. Create custom user model if needed
3. Implement email verification flow
4. Add refresh token rotation
5. Configure permission classes
6. Add rate limiting
7. Write security tests
8. Document API authentication

## Best Practices

The Django Developer agent follows these principles:

### Code Quality
- Django style guide compliance
- PEP 8 formatting with type hints
- Comprehensive docstrings
- >90% test coverage
- Security-first approach

### Architecture
- Fat models, thin views pattern
- Service layer for complex business logic
- Proper app organization
- Clear URL configuration
- Reusable components

### Performance
- Query optimization (select_related, prefetch_related)
- Database indexing strategy
- Caching (Redis, database, template)
- Async views where beneficial
- CDN for static files

### Security
- CSRF protection enabled
- XSS prevention
- SQL injection defense through ORM
- Secure cookie configuration
- HTTPS enforcement
- Rate limiting
- Security headers

## Integration with Other Agents

The Django Developer agent collaborates effectively with:

- **python-pro**: Python optimization and advanced features
- **fullstack-developer**: Full-stack integration
- **database-optimizer**: Query and schema optimization
- **api-designer**: API architecture and design patterns
- **security-auditor**: Security review and hardening
- **devops-engineer**: Deployment and infrastructure
- **frontend-developer**: API integration and coordination

## Common Workflows

### 1. New Django Project
```markdown
Initialize a new Django 4.2 project for an e-commerce platform with:
- User authentication
- Product catalog
- Shopping cart
- Payment integration
- Admin dashboard
```

### 2. API Development
```markdown
Create REST API for the Product model with:
- List/Detail/Create/Update/Delete endpoints
- Filtering by category and price range
- Pagination (100 items per page)
- JWT authentication
- Rate limiting (100 requests/hour)
```

### 3. Performance Optimization
```markdown
Optimize the slow dashboard view that shows:
- User statistics
- Recent orders
- Top products
- Revenue charts
Currently takes 3+ seconds to load.
```

### 4. Migration Management
```markdown
Create migrations for:
- Add 'slug' field to Product model
- Change Category relationship to many-to-many
- Add indexes for commonly filtered fields
```

## Testing

The agent emphasizes test-driven development:

```python
# Generated test example
from django.test import TestCase
from django.contrib.auth import get_user_model
from .models import Product

class ProductModelTest(TestCase):
    def setUp(self):
        self.user = get_user_model().objects.create_user(
            username='testuser',
            password='testpass123'
        )
        self.product = Product.objects.create(
            name='Test Product',
            price=99.99,
            owner=self.user
        )

    def test_product_creation(self):
        self.assertEqual(self.product.name, 'Test Product')
        self.assertEqual(self.product.price, 99.99)

    def test_product_str_representation(self):
        self.assertEqual(str(self.product), 'Test Product')
```

## Troubleshooting

### Migration Conflicts
The agent handles migration conflicts by:
1. Identifying conflicting migrations
2. Creating merge migrations when needed
3. Resolving dependency issues
4. Squashing migrations when appropriate

### Performance Issues
For slow queries, the agent:
1. Enables query logging
2. Analyzes query patterns
3. Applies ORM optimizations
4. Adds strategic indexes
5. Implements caching
6. Benchmarks improvements

### Security Concerns
The agent proactively:
1. Scans for common vulnerabilities
2. Applies security best practices
3. Configures security middleware
4. Implements rate limiting
5. Adds security headers
6. Reviews authentication flows

## Support and Resources

- [Django Documentation](https://docs.djangoproject.com/)
- [Django REST Framework](https://www.django-rest-framework.org/)
- [pytest-django](https://pytest-django.readthedocs.io/)
- [Celery Documentation](https://docs.celeryproject.org/)
- [Django Security Guide](https://docs.djangoproject.com/en/stable/topics/security/)

## License

MIT License - See repository for details.

## Contributing

Contributions welcome! Please submit issues and pull requests to the [Claude Code Agent Marketplace](https://github.com/anthropics/claude-code-agent-marketplace).
