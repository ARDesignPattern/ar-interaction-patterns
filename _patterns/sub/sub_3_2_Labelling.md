---
layout: pattern
title: "Labelling"
category: "sub-level"
pattern_category: presenter
order: 3.2

tags:
  - Exploration
  - Showing Details 
thumbnail: /images/Gif/Labelling.gif
summary: "Explore In-Depth Exhibit Information"
description: "Provides access to detailed information about an exhibit, particularly useful for complex or multi-faceted displays."
---

  <div class="column">
    <img src="{{ '/images/Gif/Labelling.gif' | relative_url }}" alt="AR Interaction" class="profile">
  </div> 
  
# Labelling
A system of markers or text that identifies different parts of an exhibit.


---
## Overview
- **Name**  
  Labelling
- **Intent**  
  Help visitors identify and learn about individual parts or components of an exhibit in a space-constrained environment by linking visual labels to physical elements and revealing detailed explanations on approach.

---
## Target
- **Problem**  
  Visitors are unable to access detailed knowledge about specific parts or components of an exhibit due to spatial constraints in the exhibition area.
- **Context**  
  - Exhibits often consist of multiple parts or components  
  - Exhibition spaces may be too tight to provide physical labels or panels for every element  
  - AR can overlay lightweight, context-sensitive labels in situ  
- **Use When**  
  - Visitors engage an AR “explanation” mode for component-level detail  
  - An exhibit includes several discrete parts but the physical footprint is limited  
- **Forces**  
  - **Clarity vs. Clutter**: Labels must be visible without overwhelming the scene  
  - **Precision vs. Responsiveness**: Pointing lines and proximity triggers must align accurately with components  
  - **Engagement vs. Distraction**: Detailed text should appear only on demand  
- **Consequences**  
  - **Positive**: Visitors gain targeted information; AR labels stay out of the way until needed  
  - **Negative**: Mis-alignment or sensor inaccuracy can lead to confusion; too many labels may distract if not hidden promptly  

---
## Application

### Solution
1. **Pointing Line**  
   - Render a thin, anchored line from each exhibit part/component to its virtual label.  
2. **Title Text**  
   - Place a concise title next to each line’s endpoint, using legible typography and contrasting background.  
3. **Proximity Trigger**  
   - Employ a distance sensor (or bounding-box check) around each title: when the user comes within ~1.5 m, fire the explanation.  
4. **Conditional Explanation Display**  
   - On trigger: fade in a detailed overlay panel describing the part (function, history, specifications).  
   - On exit: fade out the panel and leave only the title and line visible.

### Rationale
Pointing lines create a direct visual association between physical components and their explanations, while proximity-based reveals prevent information overload and preserve the exhibit’s visual integrity.

### Design Parameters
- **Line Thickness**: 1–2 cm   
- **Title Distance**: 0.2–0.8 m from component in 3D space  
- **Trigger Radius**: 1.2–3 m around title anchor  
- **Fade Duration**: 0.5 s for panel in/out  
<!-- - **Panel Size**: 300 × 200 px (min) for readability   -->

<!-- ### Game Mechanics
- **Explorer Badge**: Unlock after viewing explanations for all components  
- **Time Challenge**: Track how quickly users discover each part  
- **Hidden Detail**: Occasionally include an Easter-egg fact unlocked by revisiting a component   -->

### Related Pattern
<!-- - Floor Circle (proximity-based AR activation)  
- Exhibit Knowledge Trigger (micro-task to surface key concept)   -->

### Impact on Immersion
- **Enhances**: Context-related interaction enhances understanding without interfering with the overall viewing experience.  
- **Risks**: Mis-fires or mis-alignment break presence; too many active lines can distract. 

### Example
<div class="intro-video-wrapper">
  <iframe
    src="https://www.youtube-nocookie.com/embed/Vp5cDmu8t7Q"
    title="YouTube video player"
    frameborder="0"
    allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture"
    allowfullscreen
  ></iframe>
</div>
<!-- In an AR tour of a mechanical watch, a thin line connects to the “Balance Wheel” label. Approaching within 1.3 m fades in a panel explaining its role in timekeeping, then fades out when stepping back. -->

<!-- ---
## Narrative Creation in Cultural Heritage

### Visitor Behavioral Goals
- **Discover components**: Encourage visitors to notice and approach individual exhibit parts by subtly highlighting their interactive labels.  
- **On-demand learning**: Let visitors control when to view detailed explanations by moving closer to labels at their own pace.  

### AR Experience Indicators
- **Pointing lines**: Thin anchored lines from each physical component to its virtual title label.  
- **Title labels**: Concise, contrasting text that appears only when viewing is unobstructed.  

### Interactive Narrative
- **Narration Design**: Add labels to the main components of the exhibition; ensure that labels are consistent across different categories and, if necessary, classify labels based on the exhibited content.
- **Audio cue**: A soft “ding” when entering the 1.2–1.5 m proximity trigger for a component. Same when the distance from the component exceeds 2–3 metres.
- **Visual cue**: The detailed overlay panel fades in around the label upon approach, then fades out on exit.  
  

### Experience Principles
- **Precision alignment**: Ensure labels and lines accurately track components without jitter.  
- **Cognitive economy**: Keep the scene uncluttered—only one detailed panel visible at a time.  
- **Seamless reveal**: Use smooth fades (0.4 s) to show and hide panels without abrupt changes.  

### Curation Considerations
- **Sensor calibration**: Adjust trigger radius per component to avoid accidental activations.  
- **Aesthetic consistency**: Match line styles and label fonts to the exhibit’s design language.  
- **Accessibility**: Offer adjustable text size, high-contrast labels, and captioned audio for all visitors.   -->

---
## Supplementary Information

### Biography
<!-- Created by interaction designer Jonas Müller for the “Precision Mechanics” exhibit at the European Museum of Science, 2025. -->

---

## Discussion
Fine-tuning trigger distances and line assignments is critical: sensors that are too sensitive lead to constant panel flicker, while overly restrictive thresholds may hide information. Future work could allow voice-activated reveals or adaptive label sizing based on user height and viewing angle.





## Notes

This pattern supports enhanced visitor engagement by delivering contextual, space-efficient information tailored to user interest and proximity.