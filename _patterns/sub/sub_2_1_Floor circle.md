---
layout: pattern
title: "Floor circle"
category: "sub-level"
pattern_category: indicator
order: 2.1

tags:
  - Exploration
  - Spatial Trigger
thumbnail: /images/Gif/EnteringCircle.gif
summary: "Spatial Activation of AR Content"
description: "Use a proximity-triggered floor circle to attract attention and seamlessly activate AR experiences, enabling intuitive and embodied engagement."
---
# Floor Circle

---
## Overview
- **Name**  
  Floor Circle
- **Intent**  
  Provide an attention-grabbing, proximity-based AR entry point that encourages natural, embodied interaction without complex input.

---

## Target
- **Problem**  
  Visitors often struggle to distinguish AR-capable exhibits and may miss opportunities to engage at their own pace.
- **Context**  
  - Only select exhibits offer AR content, so cues must stand out.  
  - Visitors roam freely without a fixed route.  
  - Activation must feel seamless, avoiding handheld controls or intricate gestures.
- **Use When**  
  - Visitors are scanning for interactive exhibits.  
  - Approaching an AR-capable exhibit warrants a clear “entry zone.”  
  - Designers want a spatial, proximity-driven activation method.
- **Forces**  
  - **Visibility vs. Subtlety**: The circle must attract attention without obstructing sightlines.  
  - **Proximity Accuracy**: Reliable detection of user position to avoid false positives/negatives.  
  - **Multimodal Feedback**: Combining visual, audio, and animation cues to confirm activation.  
- **Consequences**  
  - **Positive**: Intuitive activation, reduced learning curve, preserves immersion.  
  - **Negative**: Overly dense trigger areas may cause the trigger to activate unexpectedly or fail to function properly; overly bright or large trigger areas may cause clutter on the ground.

---

## Application

### Solution
1. **Spatial Entry Trigger**  
   - Render a virtual circle on the floor in front of the exhibit.  
   - Use a proximity sensor: when the user’s feet enter the circle boundary, fire activation.

2. **AR Experience Indicator Interface**  
   - Above or beside the circle, display:  
     - A looping 3D model (e.g., a swimming orca).  
     - A title label in legible typography (e.g., “Orca”).  
     - Subtle pulsing or glow on the circle’s edge.

3. **Activation Mechanism**  
   - On entry:  
     - Play a spatial audio cue (chime or splash).  
     - Fade out the model, label, and circle.  
     - Voice prompt confirms launch: e.g., “Orca AR experience launched”. (Optional)

4. **Feedback Cues**  
   - Visual disappearance of interface elements.  
   - Spatialized audio confirmation.  
   <!-- - Optional quick “boot-up” animation before content begins. -->

### Rationale
Anchoring a simple visual zone to the floor leverages natural proximity behavior, reducing cognitive load and eliminating the need for manual controls. Multimodal cues ensure clear feedback without distracting from the exhibit.

### Design Parameters
- **Circle Radius**: 1.2–1.5 m to allow comfortable entry.  
<!-- - **Pulse Rate**: 0.8–1 Hz for gentle attractor effect.   -->
- **Label Height**: 0.5 m above floor to stay in peripheral view.  
<!-- - **Audio Volume**: Adjust to 60–70 dB SPL in typical gallery acoustics.   -->
- **Fade Duration (Optional)**: 0.5 s for interface elements to dissolve.

<!-- ### Game Mechanics
- **Proximity Badge**: Earn a “First Step” achievement for first-time activation.  
- **Speed Challenge**: Time from circle entry to full activation for a playful metric.  
- **Sequential Unlocks**: Visiting all circles in an exhibit set unlocks bonus content. -->

### Related Pattern
<!-- - **Avatar Guide** (character-led escort)  
- **Surface Tap Indicator** (gesture-based AR activation) -->

### Impact on Immersion
- **Enhances**: Seamless entry, embodied interaction, minimal UI overhead.  
- **Risks**: Jittery localization breaks presence; overly bold visuals detract from exhibits.

### Example
<div class="intro-video-wrapper">
  <iframe
    src="https://www.youtube-nocookie.com/embed/CtplECOaHXc"
    title="YouTube video player"
    frameborder="0"
    allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture"
    allowfullscreen
  ></iframe>
</div>
<!-- At an aquarium exhibit, a softly glowing blue circle with a pulsing orca model invites visitors forward. Stepping into the zone triggers a splash sound, the circle fades, and a narrated 3D orca appears swimming in the space before them. -->

---

## Narrative Creation in Cultural Heritage
### Visitor Behavioral Goals
- **Draw visitors in**: Define an “experience circle” on the floor in front of the exhibit so visitors instinctively step into it.  
- **Auto-start interaction**: Once inside the circle, AR content (narration or animation) begins without requiring any buttons.

### AR Experience Indicators
- **Floor marking**: Paint a low-saturation circle on the gallery floor (radius ≈ 1.3 m) that complements the exhibit’s overall design.  
- **Guiding element**: Beside the circle, place a small sign or sculpture (height ≈ 50 cm) with a prompt like “Step here to hear the whale’s story.”

### Interactive Narrative
1. **Audio cue**: As visitors enter the circle, play a soft ocean ambience or whale call at a comfortable volume.  
2. **Visual cue**: After the sound, fade out the floor marking and sign so attention shifts to the AR scene.  
3. **Narration launch**: Immediately follow with a voiceover, e.g. “Welcome to the orca exhibit”

### Experience Principles
- **Intuitive guidance**: Combine floor markings and text prompts to steer visitors along the intended path.  
- **Seamless transition**: Ensure the fade-out of markers and the appearance of AR content are smooth, with no jarring gaps.  
- **Comfortable pacing (Optional)**: Allow a brief (~0.5 s) pause before the animation or narration starts to maintain flow.

### Curation Considerations
- **Traffic flow**: Position the circle so it doesn’t block main pathways or conflict with adjacent exhibits.  
- **Aesthetic harmony**: Choose marking colors and materials that blend with floor finishes and lighting—visible yet unobtrusive.  
- **Accessibility**: Ensure visitors of all heights and those with mobility challenges can easily enter the trigger zone.

--- 
## Supplementary Information

### Biography
-


## Discussion
Balance the circle’s visibility and size to avoid both missed activations and floor clutter. Future iterations might adapt circle color or shape based on user profiles or exhibit themes.





## Notes

The Circle Indicator pattern makes AR content more accessible and discoverable through spatially grounded, low-friction interaction. By relying on embodied triggers and minimal UI, it supports intuitive engagement while preserving immersion in the exhibition space. This design is especially effective for visitors unfamiliar with gesture-based systems or those exploring independently without guidance.