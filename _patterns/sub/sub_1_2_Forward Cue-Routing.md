---
layout: pattern
title: "Forward Cue-Routing"
category: "sub-level"
pattern_category: guiding
order: 1.2

tags:
  - Exploration
  - Experience Navigation
thumbnail: /images/Gif/FollowCirclePattern.gif
summary: "Exploring and Controlling AR Content"
description: "Exploring and Controlling AR Content: Present the content in a structured, navigable, and user-controlled manner."
---
<!-- <div class="column">
  <img src="{{ '/images/Gif/FollowCirclePattern.gif' | relative_url }}" alt="AR Interaction" class="profile">
</div>  -->

# Forward Cue-Routing



---
## Overview
- **Name**  
  Forward Cue-Routing
- **Intent**  
  Provide concise, ground-based augmented reality prompts to show users upcoming turns and maintain immersion through synchronised visual ‘ripples’ and spatialised audio, while displaying the route the user has already passed.

---
## Target
- **Problem**  
  Visitors often lose situational awareness at decision points such as corners or junctions. Traditional path lines may be overlooked in visually dense AR scenes, and users may miss subtle route deviations, leading to detours and time loss.
- **Context**  
  - Feature long corridors, frequent turns, or multi-level layouts  
  - Can pre-author routes and embed triggers at discrete waypoints  
  - Require an unobtrusive, ground-anchored visual language to maintain immersion  
- **Use When**  
  - Users prefer minimal above-eye-level graphics that do not occlude exhibits  
  - Clear anticipation of turns is essential—for example, in labyrinthine galleries  
  - The institution wants a metaphor evocative of flow or movement (e.g., ripples) rather than character-based guidance  
  - Acoustic icons can be leveraged at each turn to reinforce direction without constant narration  
- **Forces**  
  - **Visual Density**: AR elements must not compete with exhibits  
  - **Anticipation vs. Reaction**: Cues must appear early enough to redirect attention  
  - **Pacing**: Visual and audio rhythms should match average walking speed  
  - **Localization Accuracy**: Ground-anchored cues rely on precise user positioning  
- **Consequences**  
  - **Positive**: Smooth, predictable navigation; high immersion; low UI clutter  
  - **Negative**: May be missed if localization jitters; requires careful tuning of cue timing and intensity  

---
## Application

### Solution
1. **Waypoint-Based Guiding**  
   - Author a polyline route with triggers at each change-of-direction node.  
   - On trigger, emit a localized cluster of visual ripples and spatialized audio.  
2. **Point of Interest Selection Interface**  
   - At the start hub, display a floor-pinned planar menu with PoI thumbnails, estimated walking time, and “Start.”  
3. **Navigation Control Interface**  
   - Invoke the start menu on demand via gesture or voice (“Show route menu”).  
   - Allow Pause/Abort; cache progress for later resumption.  
4. **Directional Visual Cues**  
   - Animate concentric “raindrop” rings on the ground, propagating toward the next waypoint.  
   - Map ring expansion rate to recommended walking speed; slow-expanding rings signal deceleration.  
5. **Auditory Feedback**  
   - Play a spatialized whoosh or bell at each turn trigger, aligned with turn direction.  
   - Adjust ambient volume based on acoustic properties of the environment.  
6. **Arrival Trigger**  
   - Converge final rings into a glowing disc at the PoI.  
   - Play a harmonic chord and pulse light to confirm arrival.

### Rationale
Ground-anchored ripples leverage peripheral vision and spatial audio to cue forthcoming turns without cluttering the user’s focus, reducing cognitive load compared to floating arrows or moving avatars.

### Design Parameters
- **Ring Expansion Rate**: Set so a ring reaches midpoint between waypoints in ~2–3 s at average walking speed (1.2 m/s)  
- **Trigger Radius**: 1–2 m before each waypoint to fire cues early  
- **Audio Lead Time**: 0.5–1 s before visual rings to pre-alert  
- **Opacity Falloff (Optional)**: Ripples fade over 1.5 s to avoid persistence  

<!-- ### Game Mechanics
- **Progress Meter**: Subtle floor bar filling toward next waypoint  
- **Time Trials**: Display a “beat the ripple” timer for more playful visits  
- **Achievements**: Unlock badges for completing routes without pausing   -->

### Related Pattern
<!-- - Avatar Guide (character-led pacing)  
- Abstract Wayfinding (floating arrows, decals)   -->

### Impact on Immersion
- **Enhances**: Maintains attention on exhibits; feels organic and thematic  
- **Risks**: Misaligned or jittery cues break presence; too-subtle rings may go unnoticed  

### Example
<div class="intro-video-wrapper">
  <iframe
    src="https://www.youtube-nocookie.com/embed/Xs7Bb4F3tq8"
    title="YouTube video player"
    frameborder="0"
    allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture"
    allowfullscreen
  ></iframe>
</div>
<!-- In a “Medieval Gallery” corridor, concentric green ripples pulse outward along the stone floor toward the next alcove. A soft chime precedes each ring sequence. Visitors instinctively follow the expanding rings and arrive at alcoves just as informative voice-overs begin. -->

<!-- ---

## Narrative Creation in Cultural Heritage

### Visitor Behavioral Goals
- **Anticipate direction**: Provide subtle early cues (ripples and audio) that draw visitors’ attention to upcoming turns before they reach decision points.  
- **Maintain flow**: Encourage continuous movement by syncing visual and auditory rhythms with average walking pace, preventing stops or confusion.  

### AR Experience Indicators
- **Ground ripples**: Animated ripple effects, such as circular/ring patterns spreading out to the next waypoint, are used to indicate direction and time. 
- **Audio icon**: Spatialized whoosh or bell sound that originates from the turn point, reinforcing the visual cue.  

### Interactive Narrative
- **Narration Design**: Present both auditory and visual narratives at each turning point so that users can experience a coherent narrative as they progress along the path.
- **Audio cue**: A directional tone plays 0.5–1 s before the ripple animation, guiding attention toward the turn.  
- **Visual cue**: Ground-anchored ripples pulse and expand in a “raindrop” fashion, mapped to walking speed.  
- **Arrival marker**: Final ripples converge into a glowing disc with a harmonic chord to signal PoI arrival.  

### Experience Principles
- **Peripheral engagement**: Use low-profile, ground-anchored visuals that register in the peripheral vision without occluding exhibits.  
- **Temporal alignment**: Time cues so that rings reach the midpoint between waypoints in 2–3 s at normal walking speed, ensuring intuitive pacing.  
- **Minimal distraction**: Keep cues subtle yet noticeable—avoid abrupt or oversized graphics that compete with the environment.  

### Curation Considerations
- **Spatial calibration**: Fine-tune trigger radii (1–2 m) and localization precision to prevent premature or delayed cues.  
- **Acoustic context**: Adjust audio volume and frequency to suit ambient noise levels and room acoustics.  
- **Accessibility options**: Offer adjustable ripple contrast, optional high-contrast overlays for hearing-impaired visitors.   -->

---

## Supplementary Information
### Biography
<!-- Developed by AR designer Li Wei for the “Time Passage” exhibition at the Beijing Museum of Digital Art, 2024. -->

## Discussion
Tuning the balance between subtlety and noticeability is key: too-fast ripples rush visitors, too-slow ones risk invisibility. Future work includes adaptive ring colors for accessibility and multi-path routing for group tours.



## Notes

Forward Cue-Routing preserves the clarity of a drawn path while avoiding visual overload in the user’s forward gaze. By anchoring cues to the floor plane and synchronising them with discrete acoustic events, the pattern balances immersion and instruction, supporting intuitive navigation even in acoustically or visually busy environments.