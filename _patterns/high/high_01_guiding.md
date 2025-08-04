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

# Point of Interest Guide
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

### Solution
1. **Path Point-Based Guiding**  
   - Author or generate a polyline route from current position to the chosen POI.  
   - Continuously update route if the user deviates or selects a new destination.  
2. **Point of Interest Selection Interface**  
   - Display a floor-pinned or HUD menu listing POIs with thumbnails, categories, and estimated travel times.  
   - Allow sorting by proximity, popularity, or remaining time.  
3. **Navigation Control Interface**  
   - Provide Start, Pause, Resume, and Cancel controls via gesture, voice, or on-screen buttons.  
   - Cache paused routes for later resumption (Optional).  
4. **Directional Visual Cues**  
   - Overlay avatar/arrows/footprints/animnated visual object along the path, shape/color-coded for upcoming turns or straight segments.  
   - Animate next-step indicators (e.g., pulsing arrow) when approaching decision points.  
5. **Auditory Feedback**  
   - Play spatialized cues at key waypoints.  
   - Adjust volume based on ambient noise and distance (Optional).  
6. **Arrival Trigger**  
   - When the user enters the POI zone, fade out path indicators, play a confirmation chime, and display a brief arrival tooltip.

### Rationale
Combining explicit path visualization with user-driven POI selection reduces cognitive load, ensures efficient coverage of highlights, and accommodates both goal-oriented and exploratory behaviors.

### Design Parameters
- **Path Width**: 1–1.5 m in AR space for clear visibility  
- **Size of the Visual Cue**: ≥ 0.3 m 
- **Distance between the cue and the user**: 1-2 m
- **Cue Lead Time (When apply)**: Announce turns 5–10 m before decision points 
<!-- - **Audio Level**: 60–70 dB SPL, adaptive to ambient noise   -->
- **Menu Reach**: Within 1-1.5 m of user gaze center for easy selection  

<!-- ### Game Mechanics
- **Explorer Badge**: Earned for visiting a sequence of POIs without pauses  
- **Time Challenge**: Complete N POIs within a time limit for a leaderboard  
- **Route Streak**: Rewards for revisiting POIs in the same order as recommended   -->

### Related Pattern
- Avatar Guide (personalized escort along a path)  
- Forward Cue-Routing (ground-anchored turn anticipation)  

### Impact on Immersion
- **Enhances**: Provides clear direction without physical signage; supports time-sensitive visits  
- **Risks**: Excessive overlays can distract; rigid routing may reduce serendipity  

### Example
<!-- At a contemporary art museum, a visitor taps the “Highlights” menu and selects “Sculpture Garden.” A translucent blue path appears on the floor, arrows pulse at each turn, and a soft voice prompts “Proceed 20 meters to the next hall.” Upon arrival, a chime sounds and the path fades, revealing the sculpture. -->

---

## Narrative Creation in Cultural Heritage

### Visitor Behavioral Goals
- **Draw visitors in**: Present a rotating carousel of featured POIs with engaging thumbnails and brief descriptions to spark curiosity.  
- **Auto-start interaction**: Automatically display the nearest POI suggestion and begin path guidance when the visitor enters the mapped area.  

### AR Experience Indicators
- **Floor marking**: Semi-transparent footprints or glowing floor tiles leading toward the selected POI.  
- **Guiding element**: A pulsing waypoint beacon (e.g., floating orb or arrow) that hovers above the path to reinforce direction.  

### Interactive Narrative
1. **Audio cue**: A gentle chime and voice prompt (“Next stop: Sculpture Garden, 50 m ahead”) as the route initializes.  
2. **Visual cue**: Animated arrows or footprints that pulse at regular intervals and brighten when a turn is imminent.  
3. **Narration design**: Short, context-sensitive voiceovers upon arrival (“Welcome to the Sculpture Garden—home to…”), with optional on-screen captions.  

### Experience Principles
- **Intuitive guidance**: Align AR cues with natural walking direction and avoid obstructing the visitor’s view of exhibits.  
- **Seamless transition**: Fade path indicators in at journey start and out upon arrival, ensuring no abrupt visual shifts.  
- **Comfortable pacing**: Announce distance and turns only when the user is within optimal lead-in range (5–10 m), avoiding clutter.  

### Curation Considerations
- **Traffic flow**: Monitor visitor density and suggest alternate routes to prevent bottlenecks at popular POIs.  
- **Aesthetic harmony**: Choose cue colors, shapes, and animations that complement the exhibit’s design language and lighting.  
- **Accessibility**: Provide high-contrast options, adjustable audio volume, and text labels to accommodate diverse visitor needs.  




---

## Supplementary Information

### Biography
Created by UX designer Elena Rossi for the “Smart Wayfinding” project at the Milan AR Museum, 2024.

---

## Discussion
Key considerations include balancing guidance granularity with user freedom, dynamically re-routing for crowd flow, and integrating predictive POI suggestions based on user interests or time constraints. Future work may incorporate group navigation modes and live occupancy data to optimize routes.


## Media



## Notes

This pattern enhances orientation and engagement in AR-rich spaces by reducing spatial confusion and supporting personalized exhibit discovery.
