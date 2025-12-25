# Mobile App Developer Agent

Expert mobile app developer specializing in native and cross-platform development for iOS and Android. Masters performance optimization, platform guidelines, and creating exceptional mobile experiences that users love.

## Overview

This agent is a senior mobile app developer with comprehensive expertise in building high-performance applications across iOS, Android, and cross-platform frameworks. It focuses on user experience, performance optimization, and platform compliance while delivering apps that delight users.

## Key Capabilities

### Native Development
- **iOS**: Swift/SwiftUI, UIKit, Core Data, CloudKit, WidgetKit, App Clips, ARKit
- **Android**: Kotlin/Jetpack Compose, Material Design 3, Room, WorkManager, CameraX

### Cross-Platform Expertise
- React Native optimization
- Flutter performance tuning
- Expo capabilities
- Platform channels and native modules

### Performance Excellence
- Launch time reduction (target: < 2 seconds)
- Memory management and battery efficiency
- App size optimization (target: < 50MB)
- Crash rate minimization (target: < 0.1%)

### Core Features
- Offline-first architecture with sync mechanisms
- Push notifications (FCM, APNS)
- Device integration (camera, location, biometrics, AR)
- Mobile security and encryption
- App store optimization and release management

## Slash Commands

### `/mobile-screen`
Design and implement a mobile screen with platform-specific UI components.

**Usage:**
```
/mobile-screen
```

**Features:**
- Platform-specific UI components (iOS/Android)
- Responsive layouts for different screen sizes
- Proper navigation integration
- Dark mode support
- Accessibility features

**Example:**
```
/mobile-screen

Please create a user profile screen with:
- Avatar image picker
- Editable text fields for name, email, bio
- Save/Cancel buttons
- Platform-appropriate styling
```

### `/mobile-test`
Set up comprehensive mobile testing strategies.

**Usage:**
```
/mobile-test
```

**Features:**
- Unit tests for business logic
- Widget/UI tests for components
- Integration tests for features
- E2E tests for critical flows
- Device-specific testing strategies
- Performance and accessibility testing

**Example:**
```
/mobile-test

Set up testing for the shopping cart feature including:
- Unit tests for cart calculations
- UI tests for add/remove items
- Integration tests for checkout flow
```

### `/mobile-performance`
Analyze and optimize mobile app performance.

**Usage:**
```
/mobile-performance
```

**Features:**
- Startup time analysis and optimization
- Memory usage profiling
- Battery efficiency improvements
- Network optimization
- Image and asset optimization
- Bundle size reduction

**Example:**
```
/mobile-performance

The app startup time is 5 seconds. Please analyze and optimize:
- Initial load performance
- Asset loading strategy
- Memory footprint
```

### `/app-store-prep`
Prepare app for store submission.

**Usage:**
```
/app-store-prep
```

**Features:**
- Metadata optimization
- Screenshot design guidelines
- Preview video recommendations
- Compliance checks
- Release notes preparation
- Beta testing strategy

**Example:**
```
/app-store-prep

Prepare my fitness tracking app for App Store submission:
- Optimize app description and keywords
- Generate screenshot templates
- Create release notes
```

## Getting Started

### Prerequisites

1. **MCP Servers**: This agent requires the following MCP servers:
   - `filesystem` - For file operations
   - `github` - For repository management
   - `context7` - For accessing up-to-date mobile development documentation
   - `memory` - For maintaining context across sessions

2. **Environment Variables**:
   - `GITHUB_TOKEN` - GitHub personal access token

### Installation

1. Copy the agent directory to your Claude Code workspace
2. Configure MCP servers using the provided `mcp-config.json`
3. Set required environment variables
4. Load the agent with Claude Code

### Configuration

The `mcp-config.json` file includes:

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
    }
  }
}
```

## Usage Examples

### Example 1: Building a New Feature

```
I need to implement a photo gallery feature with:
- Grid layout of thumbnails
- Full-screen image viewer
- Pinch-to-zoom
- Share functionality
- Offline caching

Please use platform-specific best practices for iOS and Android.
```

### Example 2: Performance Optimization

```
/mobile-performance

My app takes 4 seconds to launch and uses 200MB of memory.
Please analyze and optimize the startup sequence and memory usage.
```

### Example 3: Store Preparation

```
/app-store-prep

I'm ready to submit version 2.0 of my e-commerce app.
Help me prepare all materials for both App Store and Play Store.
```

### Example 4: Testing Setup

```
/mobile-test

Set up comprehensive testing for the authentication flow:
- Email/password login
- Social login (Google, Apple)
- Biometric authentication
- Token refresh
```

## Quality Metrics

The agent ensures apps meet these quality standards:

- **App Size**: < 50MB
- **Startup Time**: < 2 seconds
- **Crash Rate**: < 0.1%
- **Accessibility**: AAA compliant
- **Battery Usage**: Efficient
- **Memory Usage**: Optimized
- **Offline Capability**: Enabled
- **Store Guidelines**: Met

## Platform-Specific Best Practices

### iOS Development
- Follow iOS Human Interface Guidelines
- Implement proper state restoration
- Use TestFlight for beta testing
- Support latest iOS features (Widgets, App Clips)
- Optimize for different device sizes

### Android Development
- Follow Material Design 3 guidelines
- Handle Android fragmentation properly
- Use Play Console for releases
- Optimize for different screen densities
- Support Android-specific features

### Cross-Platform
- Maintain platform parity where appropriate
- Use platform-specific code when needed
- Optimize bundle sizes
- Test on both platforms thoroughly
- Follow each platform's conventions

## Integration with Other Agents

This agent collaborates with:

- **ux-designer**: Mobile UI/UX design and prototyping
- **backend-developer**: API integration and server communication
- **qa-expert**: Mobile testing and quality assurance
- **devops-engineer**: Mobile CI/CD pipelines
- **product-manager**: Feature prioritization and roadmap
- **payment-integration**: In-app purchases and payment processing
- **security-engineer**: Mobile app security and encryption

## Workflow

1. **Requirements Analysis**
   - Understand app goals and target platforms
   - Map user journeys
   - Define performance targets
   - Analyze device compatibility

2. **Implementation Phase**
   - Design architecture
   - Set up project structure
   - Implement core features
   - Optimize performance
   - Test thoroughly

3. **Launch Excellence**
   - Polish UI/UX
   - Complete accessibility features
   - Harden security
   - Prepare store listings
   - Integrate analytics
   - Set up support channels

## Best Practices

- **Start with performance in mind**: Optimize from the beginning
- **Test on real devices**: Simulators can't catch everything
- **Follow platform guidelines**: Users expect platform-native experiences
- **Handle edge cases**: Poor network, low battery, limited storage
- **Monitor continuously**: Track crashes, performance, and user behavior
- **Iterate based on feedback**: Regular updates keep users engaged
- **Prioritize accessibility**: Make apps usable for everyone
- **Secure by default**: Protect user data and privacy

## Troubleshooting

### Common Issues

**Slow Startup Time**
- Minimize work on main thread
- Lazy load resources
- Optimize image assets
- Defer non-critical initialization

**High Memory Usage**
- Profile memory allocations
- Fix memory leaks
- Optimize image handling
- Implement pagination

**Crashes**
- Set up crash reporting (Firebase, Sentry)
- Add proper error handling
- Test edge cases
- Monitor production crashes

**Poor Battery Life**
- Optimize network requests
- Reduce location accuracy when possible
- Minimize background work
- Profile energy usage

## Resources

- [iOS Human Interface Guidelines](https://developer.apple.com/design/human-interface-guidelines/)
- [Material Design 3](https://m3.material.io/)
- [React Native Documentation](https://reactnative.dev/)
- [Flutter Documentation](https://flutter.dev/)
- [Mobile Performance Best Practices](https://web.dev/mobile/)

## Support

For issues, questions, or contributions, please refer to the main Claude Code Agent Marketplace repository.

## License

This agent is part of the Claude Code Agent Marketplace and follows the repository's license terms.

---

**Note**: Always prioritize user experience, performance, and platform compliance while creating mobile apps that users love to use daily.
