# Python Pro Agent

Expert Python developer specializing in modern Python 3.11+ development with deep expertise in type safety, async programming, data science, and web frameworks.

## Overview

Python Pro is a senior Python development agent that masters Pythonic patterns while ensuring production-ready code quality. It combines expertise in web development, data science, automation, and system programming with a focus on modern best practices.

## Key Features

- **Type-Safe Development**: Complete type annotations with mypy strict mode compliance
- **Async Programming**: Expert-level AsyncIO and concurrent programming patterns
- **Web Frameworks**: FastAPI, Django, and Flask expertise with async support
- **Data Science**: Pandas, NumPy, Scikit-learn, and visualization tools
- **Testing Excellence**: Test-driven development with pytest and >90% coverage
- **Performance Optimization**: Profiling, caching, and async I/O optimization
- **Security First**: OWASP compliance, vulnerability scanning, and secure coding practices
- **Modern Tooling**: Poetry, Black, Ruff, and comprehensive quality tools

## Installation

1. Copy the `python-pro` directory to your Claude Code agents location
2. Ensure you have the required MCP servers configured (see MCP Configuration below)
3. Set up the required environment variable: `GITHUB_TOKEN`

## MCP Configuration

This agent uses the following MCP servers:

- **filesystem**: Access to local filesystem for reading/writing Python files
- **github**: GitHub integration for repository management and collaboration
- **context7**: Documentation and code context lookup for Python libraries
- **memory**: Conversation memory for maintaining project context

The MCP configuration is defined in `mcp-config.json` and will be automatically loaded when the agent is activated.

## Slash Commands

### /py-analyze

Perform comprehensive Python code analysis:
- Type coverage with mypy
- Test coverage with pytest-cov
- Code quality metrics
- Security scanning with bandit
- Complexity analysis
- Detailed improvement recommendations

**Usage**: `/py-analyze`

### /py-test

Run complete test suite:
- Execute pytest with all tests
- Generate coverage reports
- Identify untested code paths
- Fixture management review
- Test optimization suggestions

**Usage**: `/py-test`

### /py-optimize

Performance analysis and optimization:
- Profile code with cProfile
- Identify performance bottlenecks
- Memory profiling
- Algorithmic complexity analysis
- Caching strategy recommendations
- Async/await refactoring suggestions

**Usage**: `/py-optimize`

### /py-type-check

Type safety verification:
- Run mypy in strict mode
- Identify missing type hints
- Type error resolution
- Generic type improvements
- Protocol and TypedDict suggestions

**Usage**: `/py-type-check`

## Capabilities

### Pythonic Patterns
- List/dict/set comprehensions
- Generator expressions for memory efficiency
- Context managers for resource handling
- Decorators for cross-cutting concerns
- Dataclasses and protocols
- Pattern matching (Python 3.10+)

### Type System Expertise
- Complete type annotations
- Generic types with TypeVar and ParamSpec
- Protocol definitions for duck typing
- TypedDict for structured dictionaries
- Literal types and Union handling
- Mypy strict mode compliance

### Web Development
- **FastAPI**: Modern async APIs with automatic OpenAPI docs
- **Django**: Full-stack applications with ORM and admin interface
- **Flask**: Lightweight microservices
- **SQLAlchemy**: Async ORM integration
- **Pydantic**: Data validation and settings management
- **Celery**: Distributed task queues

### Data Science
- **Pandas**: Advanced data manipulation and analysis
- **NumPy**: Numerical computing and vectorization
- **Scikit-learn**: Machine learning pipelines
- **Matplotlib/Seaborn**: Data visualization
- **Jupyter**: Interactive notebook development

### Testing & Quality
- Test-driven development with pytest
- Fixtures and parameterized tests
- Mocking and patching
- Property-based testing with Hypothesis
- Coverage reporting (>90% target)
- Integration and E2E tests

## Usage Examples

### Example 1: Building a FastAPI Service

```
"Create an async FastAPI service for user management with PostgreSQL,
including Pydantic models, SQLAlchemy async ORM, authentication,
and complete test coverage."
```

The agent will:
- Set up project structure with Poetry
- Create type-safe Pydantic models
- Implement async SQLAlchemy ORM
- Build FastAPI endpoints with auth
- Write comprehensive pytest tests
- Configure mypy and ruff
- Add security scanning

### Example 2: Data Analysis Pipeline

```
"Build a data analysis pipeline that reads CSV files, performs statistical
analysis, generates visualizations, and exports results to Excel."
```

The agent will:
- Use Pandas for data manipulation
- Implement vectorized operations
- Create Matplotlib/Seaborn visualizations
- Add statistical analysis
- Include error handling
- Write unit tests
- Optimize for large datasets

### Example 3: CLI Tool Development

```
"Create a CLI tool using Click for managing project configurations with
rich terminal UI and YAML configuration support."
```

The agent will:
- Structure CLI with Click
- Add Rich for beautiful terminal output
- Implement Pydantic for config validation
- Include progress bars and logging
- Add comprehensive tests
- Configure for PyPI distribution

## Quality Standards

All code delivered by Python Pro adheres to:

- **Type Coverage**: 100% for public APIs
- **Test Coverage**: >90% with pytest
- **Code Style**: Black formatting, PEP 8 compliance
- **Linting**: Ruff with strict configuration
- **Type Checking**: Mypy strict mode
- **Security**: Bandit scanning passed
- **Documentation**: Google-style docstrings

## Integration with Other Agents

Python Pro collaborates seamlessly with:

- **frontend-developer**: Provides API endpoints and data contracts
- **backend-developer**: Shares data models and service integration
- **data-scientist**: Builds ML pipelines and data processing
- **devops-engineer**: Containerization and deployment configuration
- **typescript-pro**: API integration and type sharing

## Best Practices

1. **Start with Types**: Define clear interfaces using Protocols and TypedDict
2. **Async First**: Use async/await for I/O-bound operations
3. **Test Early**: Write tests alongside implementation (TDD)
4. **Profile Often**: Use profiling tools to identify bottlenecks
5. **Secure by Default**: Input validation, SQL injection prevention, secret management
6. **Document Thoroughly**: Google-style docstrings for all public APIs
7. **Optimize Wisely**: Vectorize with NumPy, cache with functools, lazy load when possible

## Dependencies

### Required
- Python 3.11 or higher

### Recommended Packages
- pytest, pytest-cov (testing)
- mypy (type checking)
- black (formatting)
- ruff (linting)
- bandit (security)
- poetry (dependency management)
- fastapi (web framework)
- pydantic (validation)
- pandas (data science)
- numpy (numerical computing)

## Environment Variables

- `GITHUB_TOKEN`: Required for GitHub MCP server integration

## Development Workflow

1. **Codebase Analysis**: Review project structure, dependencies, and conventions
2. **Environment Setup**: Configure virtual environment, install dependencies
3. **Implementation**: Write idiomatic, type-safe, tested Python code
4. **Quality Assurance**: Run linting, type checking, tests, and security scans
5. **Documentation**: Generate docs and usage examples
6. **Delivery**: Provide comprehensive summary of implementation

## Support

For issues, questions, or contributions, please refer to the main Claude Code Agent Marketplace repository.

## License

See the main repository for license information.
