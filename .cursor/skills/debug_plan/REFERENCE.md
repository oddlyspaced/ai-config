# Debug Plan - Investigation Techniques Reference

## Investigation Techniques

### Binary Search Debugging
When you don't know where the bug is in a long pipeline:
1. Find the midpoint of the data/execution flow
2. Check if data is correct at the midpoint
3. If correct: bug is in the second half
4. If incorrect: bug is in the first half
5. Repeat until you've isolated the exact location

### Comparison Debugging
When a feature works in one case but not another:
1. Find a working case and a broken case
2. Identify every difference between them
3. Eliminate differences one by one
4. The remaining difference is likely the cause

### Temporal Debugging (Regression)
When something used to work:
1. Find the last known working state (commit, date, deploy)
2. Use `git bisect` or manual bisection between working and broken
3. Analyze the introducing change
4. Understand intent vs. impact

### Minimal Reproduction
Simplify until the bug is obvious:
1. Start with the full reproduction
2. Remove components/steps one at a time
3. If the bug disappears, the last removed component is involved
4. If the bug remains, continue simplifying
5. The minimal reproduction reveals the essential trigger

### Rubber Duck / Trace Walkthrough
For logic bugs where "it should work":
1. Start at the entry point
2. For every line, state what happens and what the values are
3. Don't assume - verify each step
4. The bug is where your assumption diverges from reality

## Common Anti-Patterns to Avoid

| Anti-Pattern | Why It's Bad | Do This Instead |
|-------------|-------------|-----------------|
| Fix the symptom | Bug comes back in a different form | Find and fix the root cause |
| Change and pray | Wastes time, introduces new bugs | Form hypothesis, test it, then change |
| Blame the framework | Usually it's your code | Verify with minimal reproduction |
| Only read the error message | Missing context from surrounding code | Read the full stack trace and surrounding code |
| Skip reproduction | Can't verify the fix works | Always establish reproduction first |
| Fix in production | Risky, hard to revert | Fix in dev, test, then deploy |
| Ignore intermittent bugs | They get worse over time | Identify the race condition or edge case |
| Solo debug for hours | Diminishing returns after ~30 min | Ask for help, explain the problem out loud |

## Investigation Techniques by Issue Type

### For Crash/Exception:
- Read the full stack trace, noting every frame
- Inspect the throw site: what condition triggered it?
- Check inputs to the failing function: are they what you expect?
- Look upstream: who called this function and with what data?

### For Wrong Output:
- Trace data from input to output
- Find the point where actual diverges from expected
- Binary search: check the midpoint of the data pipeline
- Compare with a working case if one exists

### For Performance:
- Identify the slow operation (profiling, timing, logs)
- Check for: N+1 queries, missing indexes, unbounded loops, large payloads
- Compare against baseline: what changed?
- Measure, don't guess

### For Race Conditions:
- Identify shared mutable state
- Map the concurrency model (threads, async, workers)
- Look for: missing locks, check-then-act patterns, stale reads
- Consider ordering assumptions that might be violated

### For Regressions:
- Use `git bisect` (or manual bisection) to find the introducing commit
- Diff the introducing commit carefully
- Understand the intent of the change and why it broke things

### For Integration Issues:
- Check API contract: request format, response format, error codes
- Verify versions: is the dependency version compatible?
- Test the dependency in isolation
- Check for breaking changes in changelogs

### For Environment Issues:
- Diff configurations between working and broken environments
- Check: env vars, secrets, file permissions, OS versions, runtime versions
- Verify network: DNS, firewall, proxy, TLS certificates
- Check resource limits: memory, disk, connections, file descriptors
