# Refactoring Specialist Agent

Expert refactoring specialist mastering safe code transformation techniques and design pattern application. Specializes in improving code structure, reducing complexity, and enhancing maintainability while preserving behavior with focus on systematic, test-driven refactoring.

## Overview

The Refactoring Specialist agent is your expert partner for transforming complex, poorly structured code into clean, maintainable systems. This agent combines deep knowledge of refactoring patterns, code smell detection, and safe transformation techniques to dramatically improve code quality while preserving existing behavior.

## Key Features

### Code Smell Detection
- Identifies 20+ common code smells
- Analyzes method, class, and design-level issues
- Prioritizes refactoring opportunities
- Provides actionable recommendations

### Complexity Analysis
- Calculates cyclomatic complexity
- Measures cognitive complexity
- Tracks nesting depth
- Monitors method and class sizes
- Analyzes coupling and cohesion

### Design Pattern Application
- 15+ common design patterns
- Strategy, Factory, Observer, Decorator
- Template Method, Adapter, Composite
- Pattern-based refactoring automation

### Safe Transformation
- Test-driven refactoring approach
- Behavior preservation verification
- Incremental change management
- Comprehensive rollback procedures

## Installation

1. **Clone or download** this agent directory
2. **Configure MCP servers** in your Claude Desktop config:

```json
{
  "mcpServers": {
    "filesystem": {
      "command": "npx",
      "args": ["-y", "@modelcontextprotocol/server-filesystem", "."]
    },
    "github": {
      "command": "npx",
      "args": ["-y", "@modelcontextprotocol/server-github"],
      "env": {
        "GITHUB_PERSONAL_ACCESS_TOKEN": "your_token_here"
      }
    },
    "context7": {
      "command": "npx",
      "args": ["-y", "@context-labs/context7-mcp-server"]
    }
  }
}
```

3. **Restart Claude Desktop** to load the configuration

## Usage

### Basic Invocation

Simply mention refactoring needs in your conversation:

```
"Can you analyze this code for refactoring opportunities?"
"Help me refactor this large class into smaller, focused classes"
"Apply the Strategy pattern to this payment processing code"
```

### Slash Commands

#### /refactor-analyze
Analyze code for refactoring opportunities, code smells, and complexity metrics.

**Usage:**
```
/refactor-analyze src/services/user_service.py
/refactor-analyze src/components/
/refactor-analyze .
```

**Output:**
- Code smells detected
- Complexity metrics by file/method
- Duplication percentage and locations
- Test coverage gaps
- Prioritized refactoring recommendations

#### /refactor-pattern
Apply a specific design pattern to existing code.

**Usage:**
```
/refactor-pattern strategy src/payment_processor.py
/refactor-pattern factory src/user_factory.py
/refactor-pattern observer src/event_system.py
```

**Supported Patterns:**
- strategy
- factory
- observer
- decorator
- adapter
- template-method
- chain-of-responsibility
- composite

#### /refactor-extract
Extract method, class, or module from existing code.

**Usage:**
```
/refactor-extract method user_service.py calculate_discount
/refactor-extract class payment_handler.py StripePaymentHandler
/refactor-extract module auth.py token_validation
```

## Common Scenarios

### Scenario 1: Large Method Refactoring

```
User: "This method is 200 lines long. Help me refactor it."

Agent process:
1. Analyzes method structure and responsibilities
2. Identifies logical sections and extract points
3. Verifies test coverage
4. Extracts methods with clear names
5. Runs tests to verify behavior
6. Provides before/after metrics
```

### Scenario 2: Code Duplication Elimination

```
User: "I have the same code pattern in 5 different places."

Agent process:
1. Locates all instances of duplication
2. Identifies common patterns and variations
3. Designs appropriate abstraction
4. Extracts to shared method/class
5. Updates all call sites
6. Verifies tests pass
```

### Scenario 3: Design Pattern Application

```
User: "Apply the Strategy pattern to our payment processing."

Agent process:
1. Analyzes current payment processing code
2. Identifies algorithm variations
3. Creates strategy interface
4. Implements concrete strategies
5. Refactors client code to use strategies
6. Runs tests and validates behavior
```

### Scenario 4: Legacy Code Improvement

```
User: "This legacy code has no tests. How can we safely refactor it?"

Agent process:
1. Creates characterization tests
2. Captures current behavior
3. Identifies safe refactoring points (seams)
4. Makes small, incremental improvements
5. Adds tests progressively
6. Improves structure while maintaining behavior
```

## Refactoring Workflow

The agent follows a systematic, safe refactoring process:

### 1. Analysis Phase
- Read and analyze code structure
- Detect code smells and anti-patterns
- Calculate complexity metrics
- Check test coverage
- Assess refactoring risks
- Create prioritized plan

### 2. Implementation Phase
- Ensure test coverage
- Make small, incremental changes
- Run tests after each change
- Verify behavior preservation
- Commit frequently
- Update documentation

### 3. Validation Phase
- Run full test suite
- Check complexity improvements
- Verify performance maintained
- Review code quality metrics
- Get team feedback
- Document lessons learned

## Code Smell Catalog

### Method-Level Smells
- **Long Method** - Methods exceeding 20-30 lines
- **Long Parameter List** - More than 3-4 parameters
- **Primitive Obsession** - Over-reliance on primitives
- **Data Clumps** - Related data items appearing together

### Class-Level Smells
- **Large Class** - Classes with too many responsibilities
- **Feature Envy** - Methods using another class's data
- **Divergent Change** - Class changing for multiple reasons
- **Shotgun Surgery** - One change affects many classes

### Design Smells
- **Refused Bequest** - Subclass doesn't use parent features
- **Inappropriate Intimacy** - Tight coupling between classes
- **Message Chains** - Long chains of method calls
- **Middle Man** - Class only delegates to others

## Metrics & Targets

### Complexity Metrics
- **Cyclomatic Complexity**: Target < 10 per method
- **Cognitive Complexity**: Target < 15 per method
- **Nesting Depth**: Target < 4 levels
- **Method Length**: Target < 30 lines

### Quality Metrics
- **Code Duplication**: Target < 5%
- **Test Coverage**: Target > 80%
- **Coupling**: Minimal dependencies
- **Cohesion**: High module unity

## Design Patterns Supported

### Creational Patterns
- Factory Pattern
- Builder Pattern
- Singleton Pattern (use sparingly)
- Prototype Pattern

### Structural Patterns
- Adapter Pattern
- Decorator Pattern
- Facade Pattern
- Composite Pattern

### Behavioral Patterns
- Strategy Pattern
- Observer Pattern
- Template Method Pattern
- Chain of Responsibility Pattern

## Safety Practices

The agent enforces strict safety practices:

1. **Test Coverage First** - Never refactor without tests
2. **Incremental Changes** - One refactoring at a time
3. **Behavior Preservation** - Verify tests pass after changes
4. **Version Control** - Commit frequently with clear messages
5. **Performance Monitoring** - Benchmark critical paths
6. **Rollback Ready** - Always maintain rollback capability
7. **Documentation Updates** - Keep docs in sync with code
8. **Team Communication** - Share refactoring decisions

## Integration with Other Agents

### Collaborative Workflows

**With code-reviewer:**
- Align on coding standards
- Review refactoring approaches
- Ensure style consistency

**With legacy-modernizer:**
- Support large-scale modernization
- Apply safe transformations
- Migrate legacy patterns

**With qa-expert:**
- Coordinate test coverage
- Validate behavior preservation
- Establish quality metrics

**With performance-engineer:**
- Optimize during refactoring
- Benchmark improvements
- Apply performance patterns

## Example Output

```
Refactoring Analysis Complete

Files analyzed: 45
Code smells detected: 38

Top Issues:
1. Long Method (15 instances)
   - UserService.process_order (247 lines)
   - PaymentHandler.validate_payment (156 lines)
   - OrderController.create_order (134 lines)

2. Code Duplication (23% overall)
   - Payment validation logic (5 instances)
   - Error handling patterns (12 instances)

3. High Complexity (8 methods > 15)
   - UserService.calculate_price (cyclomatic: 28)
   - OrderProcessor.validate (cyclomatic: 19)

Recommendations:
1. Extract UserService.process_order into smaller methods
2. Create PaymentValidator class to eliminate duplication
3. Apply Strategy pattern to payment processing
4. Introduce Parameter Object for order creation

Estimated effort: 2-3 days
Risk level: Low (good test coverage at 87%)
Expected improvement: -45% complexity, -60% duplication
```

## Best Practices

### Do's
- Always ensure test coverage before refactoring
- Make one change at a time
- Commit after each successful refactoring
- Run tests after every change
- Measure improvements with metrics
- Document significant decisions
- Communicate with the team

### Don'ts
- Don't refactor without tests
- Don't make multiple changes simultaneously
- Don't skip test verification
- Don't ignore performance impacts
- Don't forget to update documentation
- Don't refactor under deadline pressure
- Don't change behavior during refactoring

## Troubleshooting

### "No test coverage exists"
The agent will help create characterization tests first:
1. Identify current behavior
2. Create tests that capture behavior
3. Verify tests pass
4. Proceed with refactoring

### "Tests failing after refactoring"
The agent will:
1. Identify what changed
2. Determine if behavior changed or test needs update
3. Roll back if behavior changed unexpectedly
4. Fix and retry

### "Performance degraded"
The agent will:
1. Run benchmarks to measure impact
2. Identify performance bottleneck
3. Apply performance optimization patterns
4. Verify improvement with metrics

## Advanced Features

### AST-Based Refactoring
- Parse code into abstract syntax trees
- Apply transformations programmatically
- Generate improved code automatically
- Preserve formatting and comments

### Cross-File Refactoring
- Rename across entire codebase
- Move classes between files
- Update all import statements
- Maintain type consistency

### Database Refactoring
- Schema normalization
- Index optimization
- Query simplification
- Migration strategies

### API Refactoring
- Endpoint consolidation
- Parameter simplification
- Versioning strategies
- Backward compatibility

## Contributing

Improvements and suggestions are welcome! Consider:
- Additional refactoring patterns
- New code smell detectors
- Enhanced metrics
- Better automation

## License

Part of the Claude Agent Marketplace. See repository license for details.

## Support

For issues, questions, or suggestions:
1. Check existing documentation
2. Review common scenarios
3. Consult the CLAUDE.md file
4. Reach out to the community

---

**Remember**: Good refactoring is safe refactoring. Always prioritize behavior preservation, test coverage, and incremental progress over speed.
