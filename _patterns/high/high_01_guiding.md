---
layout: pattern
title: "Point of Interest Guide"
category: "high-level"
pattern_category: guiding
overlay: /images/PatternIcon/Path.png
order: 1
tags:
  - Navigation
  - AR

thumbnail: /images/high_guide.png
summary: "Guiding to Points of Interest (PoIs)"
description: "To assist users in reaching PoIs effectively, combine spatial guidance, interface support, and multisensory feedback."
---
  <div class="column">
    <img src="{{ '/images/HomePage/Fig_POIGuide.png' | relative_url }}" alt="AR Interaction" class="profile">
  </div> 
# Point of Interest Guide
A spatial path or cue that directs visitors toward a point of interest.


---
## Overview
- **Name**  
  Point of Interest Guide
- **Intent**  
  Help visitors efficiently locate and navigate to selected POIs in complex AR spaces by combining path visualization, selection interfaces, and multisensory feedback.

---

## Target
- **Problem**  
  Visitors in AR-enhanced environments may miss key exhibits due to complex layouts, limited time, or insufficient physical signage.
- **Context**  
  - AR spaces with multiple dispersed POIs (museums, galleries, trade shows)  
  - Large or subdivided venues where wayfinding is non-trivial  
  - Conventional maps or signage are inadequate or hard to interpret  
- **Use When**  
  - Visitors begin exploration and need their first AR destination  
  - Visitors want to locate unvisited exhibits efficiently  
  - Visitors wish to revisit previously seen POIs  
  - Time constraints demand targeted navigation  
- **Forces**  
  - **Efficiency vs. Exploration**: Balancing guided paths with room for serendipity  
  - **Clarity vs. Clutter**: Presenting enough cues without overwhelming the AR view  
  - **Control vs. Automation**: Letting users choose destinations while automating the routing  
  - **Multisensory Consistency**: Aligning visual and audio guidance seamlessly  
- **Consequences**  
  - **Positive**: Reduced search time; improved coverage of key content; higher visitor satisfaction  
  - **Negative**: Over-directing may stifle free exploration; UI elements may occlude exhibits  

---

## Application

### Solution (High-Level, Principle-Only)
1. **Purpose & Scope**  
Orchestrate the end-to-end journey **Select → Route → Navigate → Arrive/Dwell → Resume/End** via system-level conventions. Specify **principles and agreement**, not representations, thresholds, or gesture sets. 
2. **Invariants (must always hold)**  
- Perceptible without occluding exhibits; 
- Pace-safe and comfortable; 
- Continuous orientation with recoverability; 
- Redundant multimodal feedback (≥2 channels); 
- Consistent semantics and accessibility across exhibits.
3. **Design Choices(Variation Points)**  
   - Guidance modality family: avatar/character, ground cues, HUD/overlays, audio/haptics.  
   - Routing policy: shortest, smoothest, thematic, accessible-first, crowd-aware.
   - Pacing policy: follower, leader, Fixed-Rhythm; adaptive or fixed.
   - Anticipation horizon: how early/often to pre-announce turns.
   - Persistence & visibility: always-on vs on-demand; level of detail.
4. **Decision Guidelines (Heuristics)**  
   Select variation points based on topology (corridors/open halls), crowding, noise/lighting, device capabilities, localization confidence, and visitor intent (goal- vs exploration-oriented).
5. **Integration Protocol (system-level agreement)**  
- Define states and events: **Select → Preview → Commit → Navigation → Anticipate-Turn → Turn → Arrive → Dwell → Resume/End**; 
- Exceptions and rollbacks: **Off-Route, Low-Confidence, Paused**; 
- Required data and hooks: route geometry, PoI metadata, telemetry (detection/deviation/arrival). 
- **NO** fixed shape, distance, or duration.

6. **Safety & Comfort Guards**  
Bound speed and acceleration deltas; avoid sharp turns/occlusion; provide exit/retry paths; **gracefully degrade** under low confidence.
7. **Accessibility & Inclusivity**  
Offer equivalent channels (speech/captions/high contrast/non-color coding/haptics); support hands-free modes and adjustable text/tempo.


### Rationale
- **Decouples orchestration from representation** preserving freedom while avoiding over-specification.
- **Enables extensibility and composition**, allowing new or combined sub-patterns without changing the agreement.
- **Reduces cognitive load while ensuring pace and safety** via invariants and guardrails.
- **Adapts across devices and environments**, gracefully degrading under uncertainty.
- **Fosters consistency and governance** with shared semantics and telemetry for large-scale operations.



<!-- ### Example -->
<!-- At a contemporary art museum, a visitor taps the “Highlights” menu and selects “Sculpture Garden.” A translucent blue path appears on the floor, arrows pulse at each turn, and a soft voice prompts “Proceed 20 meters to the next hall.” Upon arrival, a chime sounds and the path fades, revealing the sculpture. -->

---

<!-- ## Narrative Creation in Cultural Heritage

### Visitor Behavioral Goals
- **Draw visitors in**: Display a POI selection menu showing nearby exhibits with their names and distances, prompting users to choose a destination.    
- **Auto-start interaction (Potional)**: Automatically display the nearest POI suggestion and begin path guidance when the visitor enters the mapped area.  

### AR Experience Indicators
- **Floor marking (Optional)**: Semi-transparent AR visual elements (eg.: footprints or glowing floor tiles) leading toward the selected POI.  
- **Guiding element**: Animated visual elements/waypoint icon (e.g., an avatar or floating arrows) that hovers above the path to reinforce direction.

### Interactive Narrative
- **Narration design**: Before the guided tour begins, provide the name of the exhibit and a description of the tour content; during the path guiding, provide basic background information on the relevant exhibits; upon reaching points of interest, start the formal exhibit presentation. 
- **Audio cue**: A gentle chime and voice prompt (eg.: This tour will lead you to the Orca exhibit) as the route initializes.  
- **Visual cue**: Guide users to points of interest using interactive visual elements (such as virtual avatars or animated arrows/footprints), with designs that align with the features and style of the exhibits.

### Experience Principles
- **Intuitive guidance**: Align AR cues with natural walking direction and avoid obstructing the visitor’s view of exhibits.  
- **Seamless transition**: Fade path indicators in at journey start and out upon arrival, ensuring no abrupt visual shifts.  
- **Comfortable pacing**: Announce distance and turns only when the user is within optimal lead-in range (5–10 m), avoiding clutter.  

### Curation Considerations
- **Traffic flow**: Monitor visitor density and suggest alternate routes to prevent bottlenecks at popular POIs.  
- **Aesthetic harmony**: Choose cue colors, shapes, and animations that complement the exhibit’s design language and lighting.  
- **Accessibility**: Provide high-contrast options, adjustable audio volume, and text labels to accommodate diverse visitor needs.  
--- -->

## Supplementary Information

### Biography
<!-- Created by UX designer Elena Rossi for the “Smart Wayfinding” project at the Milan AR Museum, 2024. -->

---

## Discussion
Key considerations include balancing guidance granularity with user freedom, dynamically re-routing for crowd flow, and integrating predictive POI suggestions based on user interests or time constraints. Future work may incorporate group navigation modes and live occupancy data to optimize routes.


## Media



## Notes

This pattern enhances orientation and engagement in AR-rich spaces by reducing spatial confusion and supporting personalized exhibit discovery.
