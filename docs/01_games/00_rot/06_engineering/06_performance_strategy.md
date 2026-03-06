# Performance Strategy

## 1. Overview

Performance optimization is a critical part of game development.

The performance strategy defines how the game maintains stable frame rates while supporting complex systems such as:

- AI behavior
- environmental simulation
- rendering
- physics
- audio processing

Because ROT is a **solo-developed project**, performance strategies must prioritize:

- predictable performance
- simple optimization techniques
- minimal system complexity
- early detection of performance issues

Optimization must occur throughout development rather than only at the end.

---

# 2. Performance Targets

The game targets stable performance on mid-range PC hardware.

Recommended targets:

Target Frame Rate  
60 FPS

Minimum Acceptable Frame Rate  
45 FPS

Worst Case Frame Rate  
30 FPS

Frame time target:

16.67 ms per frame

Performance systems should be designed to remain within this budget.

---

# 3. Performance Budget

Each major system consumes part of the frame budget.

Example frame budget allocation:

Rendering  
8 ms

AI Systems  
2 ms

Physics  
2 ms

Gameplay Systems  
2 ms

Audio  
1 ms

UI  
1 ms

These values provide guidelines for balancing system workloads.

---

# 4. Early Optimization Philosophy

Optimization should begin during system design.

Important principles:

Avoid unnecessary calculations  
Avoid expensive operations in update loops  
Reuse objects whenever possible  
Prefer data-driven logic over complex runtime calculations

Good architecture prevents performance problems.

---

# 5. Level Streaming

The game world must avoid loading all content simultaneously.

Large areas should use **streaming**.

Streaming loads and unloads parts of the world as the player moves.

Example:

Player enters district
→ Load district assets

Player leaves district
→ Unload district assets

Streaming reduces memory usage and improves performance.

---

# 6. Object Pooling

Objects that spawn frequently should use pooling.

Examples include:

bullets  
particle effects  
enemy projectiles  
temporary visual effects

Instead of creating and destroying objects repeatedly, the system reuses existing objects.

Example structure:

ObjectPool
{
pooledObjects[]
activeObjects[]
}

Object pooling reduces memory allocation overhead.

---

# 7. AI Optimization

Enemy AI can become expensive if many enemies are active.

Optimization techniques include:

Distance-based AI activation  
Enemies far from the player become inactive.

Reduced update frequency  
AI logic updates less frequently than frame rate.

Simplified perception checks  
Avoid expensive calculations every frame.

Example:

AI update every 0.2 seconds

This dramatically reduces CPU usage.

---

# 8. Physics Optimization

Physics calculations must remain efficient.

Recommended strategies:

Use simple collision shapes  
Avoid complex mesh collisions  
Disable physics for inactive objects  
Use triggers instead of physics when possible

Physics objects should be limited to essential gameplay elements.

---

# 9. Rendering Optimization

Rendering is the most expensive system in most games.

Key rendering strategies include:

Level of Detail (LOD)

Distant objects use simplified models.

Occlusion Culling

Objects hidden behind geometry are not rendered.

Frustum Culling

Objects outside the camera view are not rendered.

These techniques reduce rendering load.

---

# 10. Asset Optimization

Game assets must be optimized to reduce memory usage.

Examples include:

Texture compression  
Reduced polygon counts  
Efficient shader usage  
Limited material variations

Asset guidelines must be enforced throughout development.

---

# 11. Memory Management

Efficient memory usage is critical to maintaining stable performance.

The game must avoid excessive memory allocations and fragmentation.

Key principles:

Allocate large systems at startup when possible  
Avoid allocating memory during gameplay loops  
Reuse objects using object pools  
Unload unused assets when leaving areas

Memory spikes during gameplay must be minimized.

---

# 12. Garbage Collection Strategy

Frequent memory allocation can trigger garbage collection pauses.

To avoid this:

Avoid creating temporary objects in update loops  
Reuse existing structures where possible  
Use object pooling for frequently spawned entities

Examples of systems that must use pooling:

projectiles  
enemy spawn effects  
particles  
temporary UI elements

Garbage collection events should be rare during active gameplay.

---

# 13. Audio Performance

Audio systems must avoid unnecessary overhead.

Audio performance strategies include:

Limit simultaneous audio sources  
Reuse audio emitters when possible  
Use compressed audio formats for long sounds  
Stream large music files instead of loading them entirely

Example:

Max simultaneous sound effects: 32

Excess audio sources should be culled automatically.

---

# 14. UI Performance

UI systems must remain lightweight and efficient.

Strategies include:

Avoid rebuilding UI layouts every frame  
Update UI only when values change  
Reuse UI elements instead of recreating them  
Limit expensive animations

Example:

Health bars update only when health changes.

---

# 15. CPU vs GPU Workload Balance

The game must maintain a balanced workload between CPU and GPU.

CPU-heavy systems include:

AI behavior  
physics simulation  
gameplay logic

GPU-heavy systems include:

rendering  
lighting  
post-processing effects

Optimization must ensure neither processor becomes a bottleneck.

---

# 16. Update Frequency Optimization

Not all systems must update every frame.

Some systems can update less frequently.

Example update intervals:

Enemy AI  
every 0.2 seconds

Ambient world simulation  
every 0.5 seconds

Environmental effects  
every 1 second

Reducing update frequency significantly lowers CPU usage.

---

# 17. Distance-Based System Activation

Systems should activate only when the player is nearby.

Examples include:

Enemy AI  
environmental animations  
physics simulations

Example:

Distance < 40m → full simulation
Distance < 80m → simplified simulation
Distance > 80m → disabled

This reduces unnecessary system updates.

---

# 18. Asset Streaming

Large assets must be streamed rather than loaded all at once.

Examples include:

environment textures  
large sound files  
background music  
distant environment geometry

Streaming improves load times and reduces memory usage.

---

# 19. Profiling Tools

Performance must be monitored during development.

Recommended profiling tools include:

Engine performance profiler  
CPU usage monitor  
GPU frame debugger  
memory usage analyzer

Profiling should occur regularly during development.

---

# 20. Performance Testing Workflow

Performance testing should occur throughout development.

Recommended workflow:

1. Test new features in isolated environments.
2. Measure performance impact using profiling tools.
3. Identify bottlenecks early.
4. Optimize systems before adding additional complexity.

Waiting until late development to optimize can create serious problems.

---

# 21. Stress Testing

Stress testing evaluates system limits.

Examples include:

spawning large enemy groups  
triggering many particle effects simultaneously  
loading large environments

Stress tests help identify performance bottlenecks.

---

# 22. Performance Monitoring Builds

Development builds should include performance monitoring tools.

Examples include:

FPS counter  
frame time graph  
AI system activity tracker  
memory usage display

These tools help developers quickly identify performance issues.

---

# 23. Optimization Philosophy

The project follows a simple optimization philosophy:

Design systems to be efficient from the start.  
Avoid premature complexity.  
Profile regularly.  
Optimize only when necessary.

Because ROT is a solo-developed project, systems must prioritize stability and maintainability over extreme technical complexity.

Well-structured systems naturally lead to better performance.

---