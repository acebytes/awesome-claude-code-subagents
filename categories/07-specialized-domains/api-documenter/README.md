# API Documenter Agent

Expert API documenter specializing in creating comprehensive, developer-friendly API documentation. Masters OpenAPI/Swagger specifications, interactive documentation portals, and documentation automation with focus on clarity, completeness, and exceptional developer experience.

## Overview

The API Documenter agent is designed to create world-class API documentation that enables successful integration and reduces support burden. It specializes in OpenAPI specifications, multi-language code examples, interactive portals, and comprehensive guides covering authentication, errors, versioning, and integration patterns.

## Capabilities

- **OpenAPI 3.1 Specification**: Create complete, standards-compliant API specifications
- **REST API Documentation**: Comprehensive endpoint documentation with examples
- **GraphQL Schema Docs**: Document GraphQL APIs with type definitions and queries
- **Multi-Language Examples**: Generate code samples in multiple programming languages
- **Interactive Portals**: Build try-it-out consoles and API explorers
- **Authentication Guides**: Document OAuth, API keys, JWT, and other auth methods
- **Error Documentation**: Complete error code reference with resolution steps
- **Versioning Guides**: Migration paths, breaking changes, and compatibility matrices
- **SDK Documentation**: Reference docs for client libraries and SDKs
- **Integration Tutorials**: Quick start guides and best practices

## Slash Commands

### /api-doc
Generate comprehensive API documentation for endpoints, including request/response schemas, parameters, and examples.

**Usage:**
```
/api-doc for the user authentication endpoints
```

**Output:**
- Complete endpoint documentation
- Request/response schemas
- Parameter descriptions
- Code examples
- Error responses

### /openapi-gen
Create or update OpenAPI/Swagger specification files with complete endpoint definitions and schemas.

**Usage:**
```
/openapi-gen for the entire REST API
```

**Output:**
- OpenAPI 3.1 specification file
- Schema definitions
- Security schemes
- Example values
- Reusable components

### /doc-review
Review existing API documentation for completeness, accuracy, and developer experience improvements.

**Usage:**
```
/doc-review on the current API docs
```

**Output:**
- Gap analysis report
- Completeness checklist
- Improvement recommendations
- Developer experience suggestions
- Standards compliance review

### /example-gen
Generate code examples in multiple programming languages for API endpoints and common use cases.

**Usage:**
```
/example-gen for the payment processing endpoint in Python, JavaScript, and Go
```

**Output:**
- Multi-language code samples
- Authentication examples
- Error handling patterns
- Common use cases
- Best practices

## MCP Servers

The agent uses the following MCP servers:

- **filesystem**: Read and write API documentation files
- **github**: Access API source code and issues for context
- **context7**: Retrieve up-to-date library and framework documentation
- **memory**: Store and recall API patterns and user preferences
- **fetch**: Fetch existing API documentation and examples from URLs

## Workflow

1. **API Analysis**: Query context manager for API details, review endpoints, schemas, and authentication methods
2. **Gap Analysis**: Identify documentation gaps, analyze user feedback, and assess integration pain points
3. **Documentation Creation**: Write OpenAPI specs, generate examples, create guides, and build interactive features
4. **Quality Assurance**: Validate completeness, test examples, gather feedback, and iterate improvements

## Documentation Checklist

- [ ] OpenAPI 3.1 compliance achieved
- [ ] 100% endpoint coverage maintained
- [ ] Request/response examples complete
- [ ] Error documentation comprehensive
- [ ] Authentication documented clearly
- [ ] Try-it-out functionality enabled
- [ ] Multi-language examples provided
- [ ] Versioning clear consistently

## Best Practices

### OpenAPI Specifications
- Use descriptive summaries and detailed descriptions
- Provide meaningful examples for all schemas
- Follow consistent naming conventions
- Define reusable components
- Document all security schemes
- Include proper type definitions

### Code Examples
- Cover real-world scenarios and edge cases
- Show authentication flows
- Demonstrate error handling
- Include pagination, filtering, and sorting
- Provide batch operation examples
- Document webhook handling

### Developer Experience
- Implement clear navigation
- Enable quick search functionality
- Add copy-to-clipboard buttons
- Use syntax highlighting
- Ensure responsive design
- Support offline access
- Include feedback widgets

### Documentation Automation
- Integrate with CI/CD pipelines
- Auto-generate from source code
- Validate specifications
- Check links automatically
- Sync with API versions
- Detect and notify changes

## Integration with Other Agents

- **backend-developer**: Collaborate on API design and implementation
- **frontend-developer**: Support on API integration and usage
- **security-auditor**: Work on authentication and security documentation
- **qa-expert**: Guide on testing documentation and examples
- **devops-engineer**: Help on deployment and infrastructure docs
- **product-manager**: Assist on feature and capability documentation
- **technical-writer**: Partner on integration guides and tutorials
- **support-engineer**: Coordinate on FAQs and troubleshooting guides

## Example Usage

### Documenting a New REST API

```
I need comprehensive documentation for our new payment processing API.
Please use /api-doc to create documentation for all endpoints including
authentication, webhooks, and error handling.
```

### Generating OpenAPI Specification

```
/openapi-gen for our user management API. Include all CRUD operations,
authentication schemes, and pagination parameters.
```

### Creating Multi-Language Examples

```
/example-gen for the subscription management endpoints in Python,
JavaScript, Ruby, and Go. Include authentication, error handling,
and webhook verification.
```

### Reviewing Existing Documentation

```
/doc-review on our current API documentation. Focus on completeness,
accuracy, and developer experience. Identify gaps and suggest improvements.
```

## Configuration

### MCP Configuration

The agent uses the following MCP server configuration:

```json
{
  "mcpServers": {
    "filesystem": {
      "command": "npx",
      "args": ["-y", "@modelcontextprotocol/server-filesystem", "${PWD}"]
    },
    "github": {
      "command": "npx",
      "args": ["-y", "@modelcontextprotocol/server-github"],
      "env": {
        "GITHUB_PERSONAL_ACCESS_TOKEN": "${GITHUB_TOKEN}"
      }
    },
    "context7": {
      "command": "npx",
      "args": ["-y", "@upstash/context7-mcp"]
    },
    "memory": {
      "command": "npx",
      "args": ["-y", "@modelcontextprotocol/server-memory"]
    },
    "fetch": {
      "command": "npx",
      "args": ["-y", "@modelcontextprotocol/server-fetch"]
    }
  }
}
```

### Environment Variables

- `GITHUB_TOKEN`: GitHub personal access token for accessing repositories

## Output Examples

### API Documentation Structure

```
API Documentation
├── Overview
│   ├── Introduction
│   ├── Base URL
│   ├── Authentication
│   └── Rate Limits
├── Endpoints
│   ├── Users
│   │   ├── GET /users
│   │   ├── POST /users
│   │   ├── GET /users/{id}
│   │   ├── PUT /users/{id}
│   │   └── DELETE /users/{id}
│   └── Payments
│       ├── POST /payments
│       ├── GET /payments/{id}
│       └── POST /payments/{id}/refund
├── Authentication
│   ├── API Keys
│   ├── OAuth 2.0
│   └── JWT Tokens
├── Errors
│   ├── Error Codes
│   ├── Error Messages
│   └── Resolution Steps
├── Webhooks
│   ├── Event Types
│   ├── Security
│   └── Retry Logic
└── SDKs
    ├── Python
    ├── JavaScript
    ├── Ruby
    └── Go
```

### OpenAPI Specification Sample

```yaml
openapi: 3.1.0
info:
  title: Payment Processing API
  version: 1.0.0
  description: Comprehensive payment processing and management API
servers:
  - url: https://api.example.com/v1
paths:
  /payments:
    post:
      summary: Create a payment
      description: Process a new payment transaction
      requestBody:
        required: true
        content:
          application/json:
            schema:
              $ref: '#/components/schemas/PaymentRequest'
      responses:
        '201':
          description: Payment created successfully
          content:
            application/json:
              schema:
                $ref: '#/components/schemas/Payment'
components:
  schemas:
    PaymentRequest:
      type: object
      required:
        - amount
        - currency
      properties:
        amount:
          type: integer
          description: Payment amount in cents
        currency:
          type: string
          description: Three-letter ISO currency code
```

## Success Metrics

- **Coverage**: 100% endpoint documentation
- **Examples**: 450+ code examples across 8+ languages
- **Satisfaction**: 4.7/5 developer satisfaction score
- **Support**: 67% reduction in support tickets
- **Adoption**: 94% successful integration rate
- **Quality**: OpenAPI 3.1 compliance maintained

## Tips for Best Results

1. **Provide Context**: Share API source code, existing docs, and user feedback
2. **Specify Requirements**: Mention target languages, authentication methods, and use cases
3. **Iterate**: Review generated documentation and request improvements
4. **Validate**: Test code examples and verify OpenAPI specifications
5. **Update Regularly**: Keep documentation in sync with API changes

## License

Part of the Claude Code Agent Marketplace.
