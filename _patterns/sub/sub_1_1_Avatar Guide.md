---
layout: pattern
title: "Avatar Guide"
category: "sub-level"
pattern_category: guiding
order: 1.1

tags:
  - Exploration
  - Experience Navigation
thumbnail: /images/Gif/FollowAvatar.gif
summary: "Exploring and Controlling AR Content"
description: "Exploring and Controlling AR Content: Present the content in a structured, navigable, and user-controlled manner."
---

  <div class="column">
    <img src="{{ '/images/Gif/FollowAvatar.gif' | relative_url }}" alt="AR Interaction" class="profile">
  </div> 

# Avatar Guide
A personable virtual companion that leads visitors through exhibits at a comfortable pace.

---
## Overview
- **Name**  
  Avatar Guide
- **Intent**  
  Provide a personable, pace‐regulated virtual companion that users naturally follow through a physical environment, enhancing orientation and thematic immersion beyond traditional wayfinding cues.

---
## Target
- **Problem**  
In AR-enhanced museum settings, guests can miss salient points of interest despite a preconfigured route, and planar indicators offer limited guidance for regulating walking pace or maintaining orientation when attention is divided among exhibits.
- **Context**  
  - Multiple points of interest dispersed across a nontrivial floor plan
  - Real-time user localization accurate enough to anchor and animate a virtual figure in situ
  - Desire for a more personable, dramaturgical companion experience than abstract wayfinding cues allow
- **Use When**  
  - Visitors prefer to “follow” a guide rather than decode symbolic markers
  - Maintaining a natural, steady walking pace is important for comfort
  - The venue wants to embody thematic or narrative elements (e.g., a curator avatar or historical persona)
  - The system must adjust pacing dynamically without manual speed controls
- **Forces**  
  - **Attention Split**: Balancing user focus between exhibits and navigation
  - **Pacing**: Ensuring a comfortable, consistent walking speed
  - **Orientation**: Preventing users from veering off the intended route
  - **Realism vs. Performance**: Keeping animations plausible without overloading device resources
- **Consequences**  
  - **Positive**: Increased engagement, clearer navigation, stronger thematic immersion
  - **Negative**: Potential uncanny-valley effects if avatar animations feel artificial; reliance on localization accuracy

---
## Application

### Solution
1. **Avatar & Path**  
   - Spawn a 3D avatar at the user’s position; bind its movement to the authored path.  
   - Monitor heading and speed; adjust the guide’s velocity to maintain a **2–3 m** following distance.  
   - **Pace & comfort:** Walking speed adapts to the visitor (**default 1.0 m/s**, range **0.8–1.2 m/s**) so the guide never pulls away. In crowded or narrow areas, shorten the following distance and slow slightly to keep things comfortable and safe.

2. **Kinematic Plausibility**  
   - Use inverse-kinematics and idle animations when paused or off-course.  
   - The avatar’s animation speed scales with movement speed; or use a color-coded outline/attire to reflect navigation states (e.g., green = en route, amber = paused).  
   - **Smoothness:** Avoid sudden starts/stops; keep turns and stops gentle so movement feels natural.

3. **Point-of-Interest Menu**  
   - Floating radial or list menu for selecting the next destination.  
   - Display estimated travel time based on the adaptive speed profile.  
   - **Placement:** Prefer **environment-anchored** placement (e.g., near the route start, at a stable waypoint, or a safe pull-over spot) to reduce gaze switching; **hand-anchored** is an **optional** quick-access variant when appropriate. Use large, readable targets and avoid occluding exhibits.

4. **Gesture-Activated Controls**  
   - Palm-up gesture reveals a mini hand-menu with **Start, Pause, Resume, End**.  
   - Haptic/audio confirmations for commands.  
   - **Minimal & fallback:** Keep commands minimal to avoid distraction; if gestures are unreliable, show a small environment-anchored panel with the same options.

5. **Auditory & Spatial Prompts**  
   - Spatialized vocal cues (“Turn left ahead”) and soft footstep sounds at decision points.  
   - Adjust volume/cadence in response to ambient noise and proximity.  
   - **Accessible prompts:** Pair audio with captions/icons and color-blind-safe indicators; repeat gently (e.g., every **6–10 s**) so guidance is helpful, not intrusive.

6. **Arrival Interaction**  
   - Upon reaching a PoI, the avatar stops and provides clear visual feedback.  
   - Trigger an on-screen tooltip and brief chime to affirm arrival.

7. **Composition**   
   - **Typical hand-off (optional):** After confirming arrival, the avatar **may** hand over to **Step-In Circle** (activation) → **Sequential Explanation/Labelling** (content exploration).  
   - **Separation of concerns:** These are **separate patterns**; the avatar’s role is guiding and announcing arrival, not presenting content. Use hand-offs when they improve flow; otherwise the avatar can remain idle until the visitor is ready.

8. **Failure & Fallback**  
   - **Lost or low-confidence tracking:** The avatar stays within this pattern’s logic—enter a **waiting** state and display simple, non-intrusive ground/path cues. After a short timeout, **ask the visitor** whether to continue or end; **do not auto-switch** to other patterns.  
   - **Crowded or narrow areas:** Shorten following distance and reduce speed; stop at safe pull-over spots rather than blocking others.  
   - **Hazards & restrictions:** Avoid stairs/edges and non-public areas; suggest a nearby alternative PoI if the planned path is unsafe.  
   - **Input fallback:** If gestures fail, provide an environment-anchored control panel. **End** is always available for a clean stop.  
   - **Quiet spaces:** Cap audio volume and rely on captions/icons.

<!-- <div class="column">
  <img src="{{ '/images/ExhibitMenu.jpg' | relative_url }}" alt="AR Interaction" class="profile">
</div>  

<div class="column">
  <img src="{{ '/images/FollowingTheButterfly.png' | relative_url }}" alt="AR Interaction" class="profile">
</div>  -->
### Rationale 
- A personable guide leverages people’s tendency to follow, reducing the effort of interpreting arrows or maps.  
- Adaptive pacing and comfortable following distance maintain flow across different visitors and room conditions.  
- Keeping hand-offs **optional** and pattern roles distinct avoids overloading the guide with presentation duties.  
- Staying in-pattern on loss (wait → gently prompt → ask) keeps the experience robust without surprising mode switches.

### Design Parameters 
- **Following distance:** **2–3 m** (default **2.5 m**; shorten in crowds or narrow aisles).  
- **Walking speed:** default **1.0 m/s**; adaptive range **0.8–1.2 m/s**.  
- **Arrival radius:** **≈ 2.0 m** (adjust to safe standoff from exhibits).  
- **Prompt cadence:** repeat gently every **6–10 s** if needed; cap volume in quiet rooms.  
- **State indication:** animation follows movement; optional outline/back beacon shows **en-route / paused / recover** (use color + icon for accessibility).  
- **Control/menu placement:** **environment-anchored by default** (route start, stable waypoint, safe pull-over); **hand-anchored optional** for quick access; keep targets large and readable.


### Related Pattern ###
  - -
  - -

### Impact on Immersion ###  
  - **Enhances**: Social presence via anthropomorphic guide, narrative cohesion
  - **Risks**: Breaks immersion if avatar animation or localization jitter is noticeable

### Example ###

<div class="intro-video-wrapper">
  <iframe
    src="https://www.youtube-nocookie.com/embed/UfcltoRAjKA"
    title="YouTube video player"
    frameborder="0"
    allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture"
    allowfullscreen
  ></iframe>
</div>


<!-- ---
## Narrative Creation in Cultural Heritage

### Visitor Behavioral Goals
- **Draw visitors in**: Craft an engaging opening animation or narrative hook, such as the avatar greeting guests by introducing its name; or with a brief thematic anecdote, to immediately capture attention and curiosity.  
- **Auto-start interaction (Optional)**: Automatically initiate the guide function when the visitor enters a defined proximity zone, minimizing manual setup and ensuring seamless engagement from the outset.  

### AR Experience Indicators (Optional)
- **Floor marking**: Subtle virtual footprints or glows embedded in the floor texture to reinforce the avatar’s path, offering a secondary cue without overwhelming the environment.  
- **Guiding element**: A dynamic light beam/particals or floating arrow above the avatar’s head that adjusts orientation in real time to highlight upcoming turns or split paths.  

### Interactive Narrative
- **Narration Design**: The content of the narrative should be designed to correspond with the movement of the avatar, providing different but coherent narrative content based on the avatar's location.
- **Audio cue**: 
  - Informative: While guiding, play a narration of an exhibit before the arrival.
  - Playful: provide a gentle chime or thematic sound effect plays as the visitor crosses a virtual trigger boundary, signaling the transition to the next segment.  
- **Visual cue**: 
  - Informative: Additional visual cue is NOT recommended in exhibit narration.
  - Playful: The avatar’s outline briefly pulses or changes colour (e.g., from green to amber) when a waypoint is reached or about to be passed.  


### Experience Principles
- **Intuitive guidance**: Visual and auditory signals should align with natural human instincts—such as following motion and responding to directional audio—to reduce cognitive load.  
- **Seamless transition**: Transitions between walking, pausing, and narration segments must occur without abrupt stops or lag, preserving a fluid journey.  
- **Comfortable pacing**: The avatar’s speed should adjust incrementally based on visitor movement, avoiding sudden accelerations or decelerations that could disrupt immersion.  

### Curation Considerations
- **Traffic flow**: Design path widths and timing to prevent group bottlenecks; consider staggered start zones or dynamic pacing adjustments for high-traffic periods.  
- **Aesthetic harmony**: Ensure avatar design, floor markings, and menus complement the exhibit’s visual style and lighting conditions to maintain thematic cohesion.  
- **Accessibility**: Provide alternative guidance modes (e.g., high-contrast outlines, text-only menus, adjustable narration volumes) to accommodate visitors with visual, auditory, or mobility impairments.   -->

---

## Supplementary Information
- **Biography**  
 -

### Discussion
This pattern balances technological capabilities (real-time localization, inverse-kinematics) with user experience goals (comfort, engagement). Future considerations include multi-avatar guiding for group tours and personalized narrative branching based on visitor interests.



## Notes

By anthropomorphizing wayfinding, the Avatar Guide reduces cognitive load and fosters social presence. Its adaptive pacing prevents visitor frustration caused by mismatched walking speeds, while gesture‑activated controls minimize visual clutter. The use of themed avatars can further reinforce the institution’s narrative identity.