# Environment Pipeline

# 1. Overview

The Environment Pipeline defines how environmental assets are created, organized, and integrated into the game world.

This pipeline ensures consistency across environments and prevents production issues such as:

- inconsistent scale
- unoptimized assets
- broken lighting
- asset duplication
- inefficient level construction

The pipeline standardizes the process from **concept → modeling → import → placement → optimization**.

Because ROT is a **solo-developed project**, the pipeline must emphasize:

- modular asset design
- efficient reuse of assets
- minimal technical overhead
- predictable performance

---

# 2. Environment Production Workflow

All environments follow the same production workflow.


Concept Design
↓
Blockout
↓
Modular Asset Creation
↓
Environment Assembly
↓
Lighting Pass
↓
Optimization
↓
Final Polish


Each step must be completed before moving to the next phase.

Skipping pipeline steps creates technical debt later.

---

# 3. Environment Types

The game world contains several types of environments.

Each type follows slightly different design rules.

Environment categories:

Urban Environments  
Examples:
- residential streets
- downtown areas
- industrial districts

Interior Environments  
Examples:
- buildings
- houses
- facilities

Natural Environments  
Examples:
- forests
- cliffs
- coastal areas

Underground Environments  
Examples:
- tunnels
- laboratory complexes
- underground chambers

Each category requires different asset sets.

---

# 4. Blockout Phase

The blockout phase creates the **basic layout of the environment**.

Blockouts use simple geometry to define:

- navigation paths
- room sizes
- gameplay spaces
- enemy encounter areas

Blockout geometry typically consists of:

- cubes
- planes
- primitive shapes

Blockouts must prioritize gameplay rather than visual detail.

Goals of blockout phase:

- validate player navigation
- verify level scale
- test enemy encounter placement
- confirm puzzle flow

Blockout environments should be playable before detailed assets are added.

---

# 5. Modular Asset Design

Most environment assets should be modular.

Modular assets allow environments to be assembled using reusable components.

Examples:

wall segments  
door frames  
windows  
floor tiles  
roof segments  
stairs

Benefits of modular design:

- faster level construction
- reduced asset creation time
- consistent architectural style
- improved performance through asset reuse

Modular assets must follow strict grid alignment.

---

# 6. Grid System

All modular environment assets must align to a grid.

Standard grid unit:


1 meter


Common modular sizes:

1m  
2m  
4m  
8m

Examples:

Doorway width → 1m or 2m  
Wall section → 4m  
Building height → multiples of 4m

Grid alignment ensures assets connect cleanly without gaps.

---

# 7. Environment Scale

Correct scale is essential for player immersion.

Standard scale references:

Door height → 2m  
Ceiling height → 3m  
Table height → 0.75m  
Window height → 1.2m

Player scale must always be considered when creating environment assets.

Incorrect scale can break gameplay and immersion.

---

# 8. Asset Creation Guidelines

Environment assets should follow strict guidelines.

Geometry rules:

Avoid extremely high polygon counts  
Use simple collision shapes  
Avoid unnecessary geometry

Texture rules:

Reuse texture atlases where possible  
Limit number of unique materials  
Use consistent texture resolution

Example texture sizes:

512x512 for small objects  
1024x1024 for medium objects  
2048x2048 for large assets

Large textures should be used sparingly.

---

# 9. Collision Setup

All environment assets must include collision geometry.

Collision should use simplified shapes.

Examples:

box collision for walls  
capsule collision for pillars  
simple hulls for large objects

Avoid mesh collision unless absolutely necessary.

Simplified collision improves physics performance.

---

# 10. Environment Assembly

Once modular assets are created, environments are assembled.

Assembly rules:

Snap all assets to grid  
Avoid overlapping geometry  
Maintain clear navigation paths

Environment assembly should follow the blockout layout closely.

Any changes to layout must be tested to ensure gameplay remains intact.

---

# 11. Navigation Paths

Environments must support clear player navigation.

Navigation paths should:

guide the player through the level  
avoid confusing layouts  
provide exploration opportunities

Good navigation uses environmental cues such as:

lighting direction  
architecture layout  
landmarks

These cues naturally guide players through the environment.

---

# 12. Lighting Pipeline

Lighting is one of the most important elements of environmental atmosphere in ROT.

The lighting pipeline must support both:

- gameplay readability
- horror atmosphere

Lighting must never interfere with the player's ability to navigate the environment.

The lighting workflow follows these stages:

Blockout Lighting  
Basic directional lighting used during blockout to test navigation.

Primary Lighting Pass  
Establishes main light sources in the environment.

Atmospheric Lighting Pass  
Adds mood lighting, color grading, and contrast.

Detail Lighting Pass  
Adds small localized lights such as lamps, screens, and reflections.

Optimization Pass  
Removes unnecessary lights and ensures stable performance.

---

# 13. Light Source Rules

Environmental lighting must follow consistent rules.

Primary light sources include:

- street lights
- lamps
- fluorescent fixtures
- moonlight
- emergency lighting

Secondary light sources include:

- flickering lights
- sparks
- glowing Rot growth
- computer monitors

Lights should rarely illuminate large areas evenly.

Horror environments benefit from uneven lighting and shadows.

---

# 14. Shadow Strategy

Shadows contribute heavily to environmental tension.

However, shadows are expensive for performance.

Rules for shadow usage:

Only major lights cast dynamic shadows  
Small lights use baked shadows  
Some lights use no shadows at all

Examples:

Street lamps → baked shadows  
Flashlight → dynamic shadow  
Emergency lights → no shadows

This keeps lighting visually rich while maintaining performance.

---

# 15. Rot Environmental Corruption

The Rot transforms environments visually and structurally.

Rot corruption should appear as organic growth spreading across surfaces.

Examples include:

- spiral growth patterns
- root-like tendrils
- fungal tissue clusters
- organic walls emerging from structures

Rot growth must appear integrated into the environment rather than placed on top of it.

Environmental corruption should gradually increase as the player progresses deeper into infected zones.

---

# 16. Rot Growth Placement

Rot growth must follow specific placement rules.

Common placement locations:

- wall corners
- cracks in concrete
- ceiling beams
- floors near moisture
- pipes and machinery

Rot rarely grows in open flat spaces without structural anchors.

Growth should appear as if it emerged from within the environment.

---

# 17. Level of Detail (LOD)

To maintain performance, large environment assets must use Level of Detail models.

LOD models reduce polygon count as objects become distant.

Typical LOD structure:

LOD0 → full detail  
LOD1 → reduced geometry  
LOD2 → low detail  
LOD3 → billboard or simplified mesh

LOD switching distances should be tuned carefully to avoid visible popping.

---

# 18. Occlusion Culling

Objects hidden behind other geometry should not be rendered.

Occlusion culling automatically disables rendering for objects blocked from view.

Examples:

Buildings behind walls  
Interior rooms not visible from outside  
Objects hidden behind terrain

This significantly improves rendering performance in dense environments.

---

# 19. Environment Streaming

Large environments must be divided into streaming zones.

Streaming zones load and unload assets dynamically based on player position.

Example structure:

Residential District  
Downtown District  
Harbor District  
Hospital Interior  
Forest Region

When the player enters a new zone:

- assets load in the background
- distant zones unload

Streaming prevents excessive memory usage.

---

# 20. Asset Naming Conventions

Environment assets must follow consistent naming rules.

Format:

ENV_[Category]_[ObjectName]

Examples:

ENV_Wall_Concrete_A  
ENV_Floor_Wood_B  
ENV_Door_Metal_A  
ENV_StreetLamp_A

This ensures assets remain organized within large projects.

---

# 21. Folder Organization

Environment assets should be organized by category.

Example structure:

Environment
│
├── Architecture
│   ├── Walls
│   ├── Floors
│   ├── Doors
│
├── Props
│   ├── Furniture
│   ├── Industrial
│   ├── Street
│
├── RotGrowth
│
├── Decals
│
└── Lighting

Clear organization improves development speed and reduces asset confusion.

---

# 22. Environment Optimization Pass

Before finalizing an environment, an optimization pass must occur.

Optimization tasks include:

Reducing draw calls  
Removing unused assets  
Reducing unnecessary lights  
Verifying LOD transitions  
Testing occlusion culling

Optimization must occur before final polish.

---

# 23. Environment Testing

Each environment must be tested for gameplay flow.

Testing includes:

Navigation clarity  
Enemy encounter spacing  
Puzzle visibility  
Lighting readability

Players should never feel lost due to poor level design.

---

# 24. Environment Polish

The final stage adds environmental storytelling details.

Examples include:

- scattered documents
- broken furniture
- blood stains
- abandoned equipment
- Rot growth variations

Polish gives environments a lived-in and believable feel.

Environmental storytelling is a core element of the ROT franchise.

---