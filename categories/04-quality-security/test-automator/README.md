# Test Automator Agent

> Expert test automation engineer specializing in building robust test frameworks and CI/CD integration

## Overview

The Test Automator agent specializes in designing and implementing comprehensive test automation strategies. It excels at framework development, UI/API/mobile test automation, CI/CD integration, and achieving high test coverage with fast feedback and reliable execution.

## Capabilities

### Primary Skills
- Test framework architecture and design
- UI automation (Selenium, Playwright, Cypress)
- API automation (REST, GraphQL, SOAP)
- Mobile automation (Appium, XCUITest, Espresso)
- Performance test automation (JMeter, k6)
- CI/CD pipeline integration
- Test data management and factories
- Reporting and analytics dashboards

### MCP Server Integrations

| Server | Purpose |
|--------|---------|
| filesystem | Read/write test scripts, config, and reports |
| github | Manage test repositories and track failures |
| context7 | Access application architecture and requirements |
| memory | Maintain framework patterns context |

## Usage

### Slash Commands

| Command | Description |
|---------|-------------|
| `/test-framework` | Design and setup test automation framework |
| `/automate-tests` | Convert manual tests to automated scripts |
| `/ci-integrate` | Integrate tests with CI/CD pipeline |
| `/test-report` | Generate execution and coverage reports |

### Example Prompts

```
Design and implement a Playwright-based test automation framework for our e-commerce application
```

```
Automate our REST API test suite with authentication and data-driven scenarios
```

```
Integrate our automated tests into GitHub Actions with parallel execution and failure notifications
```

```
Create a mobile test automation framework using Appium for our iOS and Android apps
```

```
Build a performance test suite for our API endpoints with load and stress scenarios
```

## Framework Design Principles

### Architecture Patterns
- **Page Object Model**: Separates UI structure from test logic
- **Data-Driven**: Parameterized tests with external data sources
- **Keyword-Driven**: Reusable action keywords for business logic
- **Screenplay Pattern**: Actor-based abstraction for complex flows
- **Hybrid Approaches**: Combination of multiple patterns

### Quality Standards
- Test coverage greater than 80%
- Execution time under 30 minutes
- Flaky test rate below 1%
- Comprehensive documentation
- Positive ROI demonstrated

## Automation Strategy

### UI Automation Best Practices
1. **Robust Locators**: Use data-testid, semantic selectors
2. **Smart Waits**: Explicit waits, retry mechanisms
3. **Cross-Browser**: Test across Chrome, Firefox, Safari, Edge
4. **Visual Regression**: Screenshot comparison and pixel diffing
5. **Accessibility**: Automated a11y checks in test suite

### API Automation Best Practices
1. **Request Validation**: Schema validation, contract testing
2. **Authentication**: Token management, session handling
3. **Data-Driven**: Parameterized tests with test data
4. **Mock Services**: Stub external dependencies
5. **Performance**: Response time benchmarks

### Mobile Automation Best Practices
1. **Cross-Platform**: Shared code for iOS and Android
2. **Device Management**: Cloud device farms, local emulators
3. **Gestures**: Tap, swipe, scroll automation
4. **Real Devices**: Test on physical devices
5. **Performance**: App startup, memory, battery metrics

## CI/CD Integration

### Pipeline Configuration
- Parallel test execution across multiple environments
- Environment-specific configuration management
- Automatic retry for flaky tests
- Test result archival and reporting
- Failure notifications to team channels

### Execution Strategy
- **Unit Tests**: Fast feedback (less than 5 minutes)
- **Integration Tests**: API and service tests (10-15 minutes)
- **E2E Tests**: Critical user journeys (15-20 minutes)
- **Full Regression**: Comprehensive suite (nightly runs)

## Test Data Management

### Strategies
- **Data Factories**: Programmatic test data generation
- **Database Seeding**: Controlled initial state
- **API Mocking**: Stub external services
- **State Management**: Isolation between tests
- **Cleanup**: Automatic teardown and reset

### Data Privacy
- Anonymized production data
- Synthetic data generation
- Secure credential management
- GDPR/compliance adherence

## Maintenance & Reliability

### Self-Healing Tests
- Automatic locator fallback strategies
- Retry mechanisms for transient failures
- Smart waiting for dynamic elements
- Error recovery and graceful degradation

### Debugging Support
- Detailed logging at each step
- Screenshots on failure
- Video recording of test execution
- Network traffic capture
- Performance metrics collection

## Reporting & Analytics

### Dashboards
- Test execution trends over time
- Pass/fail rates by test suite
- Flaky test identification
- Coverage metrics visualization
- Performance benchmarks

### ROI Metrics
- Time saved vs manual testing
- Defects caught before production
- Deployment frequency improvement
- Mean time to feedback reduction

## Requirements

### API Keys (Optional)
- `GITHUB_TOKEN` - Required for repository management
- `CONTEXT7_API_KEY` - Required for architecture context access

### CLI Tools
- Node.js 18+
- npx
- git

### Runtime Dependencies
Varies by framework choice (automatically handled by package managers)

## Best Practices

1. **Independent Tests**: Each test can run in isolation
2. **Atomic Tests**: One test, one assertion concept
3. **Clear Naming**: Descriptive test and method names
4. **Proper Waits**: Avoid sleep, use explicit waits
5. **Error Handling**: Graceful failures with clear messages
6. **Logging Strategy**: Structured logs for debugging
7. **Version Control**: All test code in Git with reviews
8. **Code Reviews**: Peer review for test quality

## Scaling Strategies

### Parallel Execution
- Multiple browser instances
- Distributed test grid
- Cloud execution platforms
- Container orchestration

### Performance Optimization
- Test prioritization and selection
- Smart test splitting
- Resource pooling
- Result caching

## Tool Ecosystem

### Popular Frameworks
- **Selenium**: Industry-standard web automation
- **Playwright**: Modern browser automation
- **Cypress**: Developer-friendly E2E testing
- **Appium**: Cross-platform mobile automation
- **RestAssured**: Java API testing
- **Supertest**: Node.js API testing
- **JMeter**: Performance and load testing
- **k6**: Modern performance testing

### CI/CD Platforms
- GitHub Actions
- GitLab CI
- Jenkins
- CircleCI
- Azure DevOps

## Collaboration

Works closely with:
- **QA Expert**: Test strategy and test case design
- **DevOps Engineer**: CI/CD pipeline integration
- **Backend Developer**: API test automation
- **Frontend Developer**: UI test automation
- **Performance Engineer**: Load and stress testing
