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

### Solution ###
1. **Avatar Instantiation & Path Binding**  
    - Spawn a 3D avatar at the user’s position; bind its movement to the authored path.
    - Monitor heading and speed; adjust guide’s velocity to maintain a 2–3 m following distance.
2. **Kinematic Plausibility**  
    - Use inverse-kinematics and idle animations when paused or off-course.
    - The avatar's animation speed is directly proportional to its the movement speed; Or, colour-code avatar outline or attire to reflect navigation states (eg.: green = en route, amber = paused).
3. **Point-of-Interest Menu**  
    - Floating radial or list menu for selecting next destination.
    - Display estimated travel time based on adaptive speed profile.
4. **Gesture-Activated Controls**  
    - Palm-up gesture reveals a mini hand-menu with Start, Pause, Resume, End.
    - Haptic/auditory confirmation for commands.
5. **Auditory & Spatial Prompts**  
    - Spatialized vocal cues (“Turn left ahead”) and footstep sounds at decision points.
    - Adjust volume/cadence in response to ambient noise and proximity.
6. **Arrival Interaction**  
    - Upon reaching a PoI, avatar stops and provides visual feedback.
    - Trigger on-screen tooltip and chime to affirm arrival.

<!-- <div class="column">
  <img src="{{ '/images/ExhibitMenu.jpg' | relative_url }}" alt="AR Interaction" class="profile">
</div>  

<div class="column">
  <img src="{{ '/images/FollowingTheButterfly.png' | relative_url }}" alt="AR Interaction" class="profile">
</div>  -->
### Rationale ###
  - Anchoring a virtual guide in situ leverages social following instincts, reducing cognitive load compared to abstract markers.
  - Adaptive pacing preserves visitor comfort and flow, preventing bottlenecks or rushed experiences.
  - Gesture controls and contextual cues keep the interface hands-free and intuitive, minimizing distraction.

### Design Parameters ###
  - **Following Distance(between the avatar and the user)**: 2–3 m  
  - **Avatar moveing speed**: Avatar's moving speed is proportional to user's walking speed; or,  around 1.2 m/s, with adjustable ±25%
  - **State Indication**: Speed-automatic-adjustable animation design.
  - **Postion of the Guiding Control Interface**: The interface anchors itself to the user's hand (as a palm menu) or to the starting point of the guidance path.


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