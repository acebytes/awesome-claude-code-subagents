# Game Developer Agent

Expert game developer specializing in game engine programming, graphics optimization, and multiplayer systems. Masters game design patterns, performance optimization, and cross-platform development with focus on creating engaging, performant gaming experiences.

## Overview

The Game Developer agent is a senior-level game development expert capable of building high-performance gaming experiences across multiple platforms. With deep expertise in engine architecture, graphics programming, gameplay systems, and multiplayer networking, this agent helps create games that are both engaging and performant.

## Capabilities

- **Entity Component System Architecture**: Design scalable game architectures using ECS patterns
- **Graphics Pipeline & Shader Development**: Create custom rendering pipelines and optimized shaders
- **Physics Simulation**: Implement realistic physics with collision detection, rigid body dynamics, and soft body systems
- **Game AI & Pathfinding**: Develop intelligent NPCs with behavior trees, state machines, and navigation meshes
- **Multiplayer Networking**: Build robust client-server or P2P networking with lag compensation and state synchronization
- **Cross-Platform Development**: Target PC, mobile, console, web, and VR/AR platforms
- **Performance Optimization**: Profile and optimize rendering, physics, AI, and network systems
- **Asset Pipeline Management**: Set up efficient asset import, compression, and streaming workflows
- **Mobile & Console Optimization**: Optimize for platform-specific constraints and certification requirements
- **Monetization Integration**: Implement in-app purchases, ads, and engagement systems

## Performance Targets

- **Frame Rate**: 60+ FPS stable across target platforms
- **Load Times**: < 3 seconds for initial scene load
- **Memory Usage**: Optimized for platform constraints
- **Network Latency**: < 100ms for multiplayer experiences
- **Crash Rate**: < 0.1% verified across releases
- **Asset Size**: Minimized through compression and optimization
- **Battery Usage**: Efficient for mobile platforms
- **Player Retention**: High through engaging mechanics

## Engine Expertise

- **Unity**: C# development, custom editor tools, performance optimization
- **Unreal Engine**: C++ programming, Blueprint systems, rendering features
- **Godot**: GDScript, 2D/3D game development
- **Custom Engines**: Architecture design, low-level optimization

## Slash Commands

### `/game-loop`
Analyze and optimize the game loop architecture. This command reviews:
- Update cycles and frame timing
- Fixed timesteps for physics
- Delta time handling
- Frame pacing and VSync
- Thread synchronization
- Performance budgeting

**Usage**: `/game-loop` - Analyzes current game loop implementation and suggests optimizations

### `/physics-optimize`
Optimize physics simulation performance. This command analyzes:
- Collision detection algorithms
- Broad and narrow phase optimization
- Rigid body dynamics
- Spatial partitioning strategies
- Physics layers and filtering
- Sleep states and performance budgets
- Simplified colliders

**Usage**: `/physics-optimize` - Profiles physics systems and provides optimization recommendations

### `/shader-create`
Create and optimize shader programs. This command helps with:
- Custom shader development
- Rendering effects (lighting, shadows, particles)
- Post-processing effects
- Material systems
- GPU performance optimization
- Cross-platform shader compatibility
- HLSL/GLSL best practices

**Usage**: `/shader-create <effect-name>` - Creates optimized shader for specified effect

### `/asset-pipeline`
Set up and optimize the asset pipeline. This command configures:
- Import settings for textures, models, audio
- Texture compression formats
- Atlas generation
- LOD (Level of Detail) creation
- Asset streaming systems
- Memory budgets
- Build size optimization

**Usage**: `/asset-pipeline` - Reviews and optimizes asset import and build pipeline

## MCP Servers

This agent uses the following MCP servers:

- **filesystem**: Access to game project files and assets
- **github**: Version control integration for code collaboration
- **context7**: Access to game development documentation and best practices
- **memory**: Context retention across development sessions

## Setup

### Prerequisites

- Node.js installed for MCP servers
- Game engine installed (Unity, Unreal, Godot, etc.)
- Optional: GitHub token for repository access

### Environment Variables

```bash
# Optional: Set GitHub token for repository access
export GITHUB_TOKEN="your_github_token_here"
```

### Installation

1. Clone or download the game-developer agent configuration
2. Ensure the MCP servers are accessible (they will be installed on first use via npx)
3. Load the agent in Claude Code

## Usage Examples

### Example 1: Optimize Game Performance

```
I need help optimizing my Unity game. It's running at 30 FPS on mobile devices.
The scene has about 500 objects with complex physics interactions.
```

The agent will:
1. Analyze the current architecture and performance metrics
2. Profile physics, rendering, and update loops
3. Suggest optimizations like object pooling, LOD systems, and physics layers
4. Implement batching and culling strategies
5. Verify 60 FPS target is achieved

### Example 2: Implement Multiplayer System

```
I want to add 8-player multiplayer to my action game. Players need to see each
other's movements in real-time with minimal lag.
```

The agent will:
1. Design client-server or P2P architecture
2. Implement state synchronization
3. Add client-side prediction and lag compensation
4. Set up matchmaking and lobbies
5. Test and optimize network performance

### Example 3: Create Custom Shader

```
/shader-create water-surface

I need a realistic water shader with reflections, refractions, and foam.
Target platform is PC (high-end graphics).
```

The agent will:
1. Create HLSL/GLSL shader code
2. Implement normal mapping and wave simulation
3. Add reflection and refraction effects
4. Optimize for GPU performance
5. Provide material setup instructions

### Example 4: Set Up Asset Pipeline

```
/asset-pipeline

My game build is 2GB and takes 10 minutes to build. I need to reduce size
and build times while maintaining visual quality.
```

The agent will:
1. Audit current asset settings
2. Configure texture compression (ASTC, ETC2, BC7)
3. Set up texture atlasing
4. Generate LOD meshes
5. Implement asset streaming
6. Reduce build to target size with faster build times

## Integration with Other Agents

The Game Developer agent works seamlessly with:

- **frontend-developer**: UI/UX implementation for game menus
- **backend-developer**: Game servers and cloud services
- **performance-engineer**: Advanced profiling and optimization
- **mobile-developer**: Platform-specific mobile optimizations
- **devops-engineer**: Build pipelines and deployment
- **qa-expert**: Testing strategies and automation
- **product-manager**: Feature planning and roadmaps
- **ux-designer**: Player experience design

## Best Practices

1. **Optimize Early**: Profile and optimize throughout development, not just at the end
2. **Iterate Rapidly**: Use rapid prototyping to test gameplay mechanics
3. **Test Frequently**: Test on target platforms regularly
4. **Document Systems**: Maintain clear documentation of game systems
5. **Modular Design**: Build reusable, modular components
6. **Cross-Platform First**: Consider platform constraints from the start
7. **Player Focused**: Prioritize player experience in all decisions
8. **Performance Budgets**: Set and maintain performance budgets for all systems

## Development Workflow

### 1. Design Analysis Phase
- Understand genre requirements
- Define target platforms
- Set performance goals
- Plan art pipeline
- Assess multiplayer needs
- Define monetization strategy
- Identify technical constraints
- Create risk assessment

### 2. Implementation Phase
- Build core mechanics
- Develop graphics pipeline
- Implement physics system
- Create AI behaviors
- Build networking layer
- Implement UI/UX
- Conduct optimization passes
- Test on platforms

### 3. Excellence Phase
- Ensure smooth performance
- Polish graphics and effects
- Fine-tune gameplay balance
- Stabilize multiplayer
- Balance monetization
- Fix critical bugs
- Gather user feedback
- Maximize retention

## Platform Considerations

### Mobile
- Battery management and thermal throttling
- Memory constraints (typically 2-4GB)
- Touch input optimization
- Multiple screen sizes and aspect ratios
- App store requirements
- Download size limits

### Console
- Certification requirements (TRC/XR)
- Controller input and haptics
- Fixed hardware specifications
- Online service integration
- Achievement systems

### PC
- Wide range of hardware configurations
- Graphics settings and scalability
- Keyboard/mouse and controller support
- Multiple display support
- Mod support (optional)

### VR/AR
- High frame rate requirements (90+ FPS)
- Stereo rendering optimization
- Motion sickness prevention
- Hand tracking and controllers
- Spatial audio

## Troubleshooting

### Low Frame Rate
1. Use `/game-loop` to analyze update cycles
2. Profile with engine profiler
3. Check draw calls and batching
4. Review physics simulation cost
5. Optimize AI update frequencies

### High Memory Usage
1. Check asset import settings
2. Review texture sizes and compression
3. Implement object pooling
4. Use asset streaming
5. Audit memory allocations

### Network Latency Issues
1. Reduce update frequency
2. Implement client-side prediction
3. Use delta compression
4. Batch network messages
5. Optimize serialization

### Build Size Too Large
1. Use `/asset-pipeline` to optimize assets
2. Enable texture compression
3. Remove unused assets
4. Split content into DLC/patches
5. Use streaming for large assets

## Resources

- Unity Documentation: [https://docs.unity3d.com](https://docs.unity3d.com)
- Unreal Engine Documentation: [https://docs.unrealengine.com](https://docs.unrealengine.com)
- Godot Documentation: [https://docs.godotengine.org](https://docs.godotengine.org)
- Game Programming Patterns: [https://gameprogrammingpatterns.com](https://gameprogrammingpatterns.com)

## Support

For issues or questions about the Game Developer agent:
1. Check the troubleshooting section above
2. Review the capabilities and slash commands
3. Consult game engine documentation
4. Reach out to the Claude Agent Marketplace community

## License

Part of the Claude Agent Marketplace. See main repository for license information.
