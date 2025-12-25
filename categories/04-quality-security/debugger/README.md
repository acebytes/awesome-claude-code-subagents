# Debugger Agent

> Expert debugger specializing in complex issue diagnosis, root cause analysis, and systematic problem-solving

## Overview

The Debugger agent specializes in diagnosing complex software issues, analyzing system behavior, and identifying root causes through systematic debugging techniques. It masters debugging tools and methodologies across multiple programming languages and platforms, with focus on efficient issue resolution and knowledge transfer to prevent recurrence.

## Capabilities

### Primary Skills
- Complex issue diagnosis and root cause analysis
- Systematic debugging across languages and platforms
- Memory debugging (leaks, corruption, buffer overflows)
- Concurrency issue resolution (race conditions, deadlocks)
- Performance debugging and profiling
- Production debugging with non-intrusive techniques
- Stack trace and core dump analysis
- Error pattern detection and correlation

### MCP Server Integrations

| Server | Purpose |
|--------|---------|
| filesystem | Read/write debug logs and postmortem documents |
| github | Track bugs and document resolutions |
| context7 | Access codebase context for debugging |
| memory | Maintain debugging history and patterns |

## Usage

### Slash Commands

| Command | Description |
|---------|-------------|
| `/debug` | Start systematic debugging session for reported issue |
| `/root-cause` | Perform deep root cause analysis on complex bug |
| `/trace` | Trace execution flow and identify failure points |
| `/postmortem` | Create comprehensive postmortem document |

### Example Prompts

```
Debug the intermittent crash in the payment processing service
```

```
Investigate memory leak causing production OOM errors
```

```
Find the race condition causing data corruption
```

```
Trace why the API returns 500 errors under high load
```

```
Create a postmortem for yesterday's outage
```

## Debugging Methodology

### Diagnostic Approach
1. **Symptom Analysis**: Gather and analyze error symptoms and patterns
2. **Hypothesis Formation**: Develop testable theories about root causes
3. **Systematic Investigation**: Apply debugging techniques to isolate issues
4. **Evidence Collection**: Gather logs, traces, and reproduction data
5. **Root Cause Identification**: Pinpoint exact cause with clear evidence
6. **Solution Validation**: Verify fix works and doesn't introduce side effects
7. **Knowledge Capture**: Document findings for future reference

### Debugging Techniques
- **Breakpoint Debugging**: Step through code execution interactively
- **Log Analysis**: Correlate logs across services and time
- **Binary Search**: Divide problem space to isolate issues
- **Divide and Conquer**: Break complex problems into manageable parts
- **Time Travel Debugging**: Replay execution backwards and forwards
- **Differential Debugging**: Compare working vs failing scenarios
- **Statistical Debugging**: Use sampling for production issues

## Specialized Debugging Areas

### Memory Debugging
- Memory leak detection and tracking
- Buffer overflow identification
- Use-after-free detection
- Double free prevention
- Memory corruption analysis
- Heap and stack analysis
- Reference tracking

**Tools**: Valgrind, AddressSanitizer, memory_profiler, heap snapshots

### Concurrency Issues
- Race condition identification
- Deadlock detection and resolution
- Thread safety verification
- Synchronization bug fixes
- Timing issue diagnosis
- Resource contention analysis

**Tools**: ThreadSanitizer, race detector, thread dumps, synchronization profilers

### Performance Debugging
- CPU profiling and hotspot identification
- Memory profiling and optimization
- I/O bottleneck analysis
- Database query performance
- Cache miss analysis
- System call tracing

**Tools**: perf, gperftools, py-spy, Chrome DevTools, Flight Recorder

### Production Debugging
- Live debugging with minimal impact
- Non-intrusive diagnostic techniques
- Distributed tracing across services
- Log aggregation and correlation
- Metrics correlation
- Canary and A/B test analysis

**Tools**: dtrace, eBPF, distributed tracing systems, APM tools

## Tool Expertise

### Interactive Debuggers
- **GDB/LLDB**: C/C++/Go/Rust debugging with breakpoints and inspection
- **Chrome DevTools**: JavaScript debugging with performance profiling
- **pdb/ipdb**: Python interactive debugging
- **Visual Studio Debugger**: .NET debugging and diagnostics
- **delve**: Go-specific debugger
- **jdb**: Java debugging

### Profilers
- **perf**: Linux performance profiling
- **Valgrind**: Memory error detection and profiling
- **gperftools**: CPU and heap profiling
- **py-spy**: Python sampling profiler
- **Java Flight Recorder**: JVM profiling
- **DTrace/eBPF**: System-level tracing

### Analysis Tools
- **strace/dtrace**: System call tracing
- **lsof**: File descriptor analysis
- **tcpdump/wireshark**: Network packet analysis
- **journalctl**: System log analysis
- **core dump analyzers**: Post-mortem debugging

## Requirements

### API Keys (Optional)
- `GITHUB_TOKEN` - Required for bug tracking and issue management
- `UPSTASH_VECTOR_REST_URL` - Optional for codebase context
- `UPSTASH_VECTOR_REST_TOKEN` - Optional for codebase context

### CLI Tools
- Node.js 18+
- npx
- git
- Language-specific debuggers (gdb, lldb, pdb, etc.)

## Common Bug Patterns

### Logic Errors
- Off-by-one errors
- Incorrect boundary conditions
- Missing null checks
- Type mismatches
- Unhandled edge cases
- State machine errors

### Resource Issues
- Memory leaks
- File descriptor leaks
- Connection pool exhaustion
- Thread leaks
- Resource deadlocks

### Concurrency Bugs
- Race conditions
- Deadlocks and livelocks
- Thread safety violations
- Improper synchronization
- Atomic operation issues

### Integration Issues
- API contract mismatches
- Version incompatibilities
- Configuration errors
- Environment differences
- Network failures

## Debugging Strategies

### For Intermittent Bugs
1. Add comprehensive logging
2. Increase log verbosity temporarily
3. Use statistical sampling
4. Analyze timing patterns
5. Check environmental factors
6. Review concurrent operations
7. Monitor resource usage

### For Production Issues
1. Minimize system impact
2. Use sampling profilers
3. Enable feature flags for gradual rollout
4. Correlate with recent deployments
5. Check monitoring dashboards
6. Review configuration changes
7. Analyze distributed traces

### For Performance Regressions
1. Bisect version history to find regression point
2. Compare performance profiles before/after
3. Analyze resource usage patterns
4. Check algorithm or data structure changes
5. Review database query changes
6. Examine cache behavior
7. Profile critical code paths

## Quality Standards

The agent ensures:
- Issue reproduced consistently before investigation
- Root cause identified with clear evidence
- Fix validated thoroughly with comprehensive tests
- Side effects and edge cases checked
- Performance impact assessed
- Documentation updated completely
- Knowledge captured systematically
- Prevention measures implemented

## Postmortem Process

After resolving critical issues, the agent creates comprehensive postmortems:

1. **Timeline**: Reconstruct sequence of events
2. **Root Cause**: Identify underlying cause with evidence
3. **Impact Assessment**: Document scope and severity
4. **Resolution**: Describe fix and validation
5. **Action Items**: List follow-up tasks
6. **Prevention**: Recommend safeguards and monitoring
7. **Lessons Learned**: Capture knowledge for team

## Best Practices

1. **Reproduce First**: Always get reliable reproduction before investigating
2. **Question Assumptions**: Verify what you think you know
3. **Think Systematically**: Use scientific method, not random changes
4. **Document Everything**: Track hypotheses, tests, and findings
5. **Understand Before Fixing**: Know why it fails, not just how to fix
6. **Test Thoroughly**: Validate fix works without breaking anything
7. **Share Knowledge**: Help team learn from the investigation
8. **Prevent Recurrence**: Add tests, monitoring, and safeguards

## Language-Specific Debugging

### JavaScript/TypeScript
- Chrome DevTools mastery
- Async/Promise debugging
- Memory leak detection
- Source map debugging
- Node.js heap snapshots

### Python
- pdb/ipdb interactive debugging
- Memory profiling with memory_profiler
- Asyncio debugging
- Exception chaining analysis
- C extension debugging

### Java
- JVM debugging with thread dumps
- Heap dump analysis
- GC log analysis
- Flight Recorder profiling
- VisualVM diagnostics

### Go
- delve debugger
- pprof profiling
- Race detector
- Goroutine leak detection
- Execution tracer

### C/C++
- GDB/LLDB mastery
- Valgrind for memory issues
- AddressSanitizer
- ThreadSanitizer
- Core dump analysis

### Rust
- LLDB with rust-lldb
- Compiler error analysis
- Lifetime debugging
- Unsafe code review
- Memory safety verification

## Collaboration

Works closely with:
- **QA Expert**: Test case creation and reproduction
- **Code Reviewer**: Fix validation and code quality
- **Performance Engineer**: Performance issue resolution
- **Security Auditor**: Security bug analysis
- **Incident Responder**: Production issue investigation
- **SRE Engineer**: Monitoring and alerting
- **Backend/Frontend Developers**: Code fix implementation

## Knowledge Management

### Bug Database
The agent maintains categorized knowledge of:
- Common bug patterns and symptoms
- Resolution strategies by issue type
- Root cause analysis examples
- Prevention techniques
- Code examples and fixes
- Tool usage guides

### Prevention Measures
After each resolution, the agent recommends:
- Code review focus areas
- Testing improvements
- Monitoring enhancements
- Alert creation
- Documentation updates
- Team training topics
- Tool automation opportunities
