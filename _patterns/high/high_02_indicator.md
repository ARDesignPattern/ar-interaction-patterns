---
layout: pattern
title: "Experience Indicator"
category: "high-level"
pattern_category: indicator
overlay: /images/PatternIcon/Initial Node.png
order: 2
tags:
  - Indication
  - AR Experience
  - AR Effects
thumbnail: /images/high_indicator.png
summary: "Recognizing and Activating AR Exhibit"
description: "Recognizing and Activating AR Experiences: To help visitors easily identify and access AR content, combine clear visual cues with intuitive activation methods and feedback."
---
  <div class="column">
    <img src="{{ '/images/HomePage/Fig_ExperienceIndicator.png' | relative_url }}" alt="AR Interaction" class="profile">
  </div> 
  
# Experience Indicator
A visual or symbolic hint that shows how to activate AR content at an exhibit.

---
## Overview
- **Name**  
 AR Experience Indicator
- **Intent**  
  Help visitors discover and launch embedded AR experiences by providing clear, consistent cues and intuitive activation methods.

---

## Target
- **Problem**  
  Visitors often don’t know which exhibits contain AR content or how to start it, causing missed opportunities and wasted time.
- **Context**  
  - Only some exhibits feature AR experiences  
  - Visitors use head-mounted displays or AR-capable devices  
  - There are no obvious physical markers denoting interactivity  
- **Use When**  
  - Visitors explore freely in a point of interest and need discoverable markers for AR-enabled exhibits  
  - Upon reaching an exhibit, users want to access rich multimedia or contextual overlays  
- **Forces**  
  - **Discoverability vs. Distraction**: Indicators must stand out without cluttering the scene  
  - **Consistency vs. Flexibility**: Use a uniform visual language while supporting varied activation methods  
  - **Immediate Feedback vs. Subtlety**: Confirm activations clearly but avoid jarring transitions  
  - **Accessibility**: Cues and activation must work across device types and user abilities  
- **Consequences**  
  - **Positive**: Increases AR uptake; reduces user frustration; highlights interactive content  
  - **Negative**: Overuse of indicators can overwhelm; inconsistent placement breaks visiting/learning expectations  

---

## Application

### Solution (High-Level, Principle-Only)
1. **Purpose & Scope**  
   Define a **platform convention** that governs the visitor journey from discovery → approach → activation. Specify **principles and agreements (i.e., system-level guarantees)**, rather than visuals, parameters, or gestures.  
2. **Invariants (must always hold)**  
   guides the visitor journey **from discovery → approach → activation. Specify 
- Discoverable without clutter.
- Clear state progression.
- Redundant, multimodal feedback (at least two channels).
- Accessible alternatives for varied abilities and contexts.
- Consistent semantics across exhibits.
3. **Design Choices(Variation Points)**  
- Placement strategy: ambient discovery vs. local anchor.
- Activation modes (e.g., proximity-based, intent-based): proximity, explicit intent, voice/assisted, etc.
- Feedback mix and intensity: visual / audio / haptic.
- Persistence level: always-on vs. on-demand; level of detail.
- Adaptation: personalization by crowding, lighting, or device capability.
4. **Decision Guidelines (Heuristics)**  
Select variation points based on spatial constraints, crowd density, safety, learning intent (concept-first vs. flow-preserving), and device/ambient limitations.
5. **Integration Protocol (system-level agreement)**  
- Define lifecycle events and analytics hooks: **Discover → Candidate (potential AR target detected) → Confirm → Activate → Exit/Recover**.
- Do **NOT** fix shapes, distances, timings, or gesture sets—those belong to sub-level patterns.

### Rationale
- **Preserves creative flexibility** by separating **what** the indicator system guarantees from **how** it is realized.
- **Enables extensibility**: new sub-level patterns can be authored without modifying the high-level contract.
- **Maintains consistency and accessibility** across exhibits while adapting to diverse spaces, devices, and audiences.
- **Supports governance and iteration** via shared lifecycle events and metrics rather than fixed UI details.



<!-- ### Game Mechanics
- **First-Use Badge**: Unlock “AR Explorer” on first activation  
- **Activation Streak**: Reward successive AR launches without pauses  
- **Discovery Tracker**: Show percentage of AR-enabled exhibits visited   -->

### Related Pattern
Sub-level patterns (e.g., Floor Circle, Exhibit Knowledge Trigger) **instantiate** choices along the variation points. They are examples, not the exhaustive set.



<!-- ### Example -->
<!-- In an art gallery, each painting with AR layers has a floating “AR” cube icon at upper right. Visitors fix their gaze on the cube for 1.5 seconds and hear a soft chime as the AR overlay loads, revealing animated brush-stroke breakdowns. -->

---
<!-- ## Narrative Creation in Cultural Heritage

### Visitor Behavioral Goals
- **Draw visitors in**: Highlight floating AR icons with a gentle glow to signal interactivity and pique curiosity.  
- **Auto-start interaction**: Automatically reveal the nearest AR indicator and enable gaze/gesture activation when a visitor approaches within 1.5-2 m.  

### AR Experience Indicators
- **Floor marking**: A subtle, semi-transparent circle at the exhibit base that appears on proximity to denote interactive zones.  
- **Guiding element**: A pulsing “AR” cube or 3D model of the exhibit hovering beside the exhibit, oriented toward the visitor’s view.  

### Interactive Narrative
- **Narration design**: Provide exhibition titles and 3D objects to present the first impression of the exhibition.
- **Audio cue**: A soft chime and brief spoken prompt (“step into to continue”) when the indicator appears.  
- **Visual cue**: The icon disappear once on activation; or smoothly transitions into the AR content overlay.  


### Experience Principles
- **Intuitive guidance**: Use consistent iconography and placement so visitors immediately recognize AR-enabled exhibits.  
- **Seamless transition**: Fade indicators in on approach and fade out once content loads, avoiding abrupt visual shifts.  
- **Comfortable pacing (Optional)**: Allow a 1–2 second dwell time for gaze selection, avoiding rushed activations.  

### Curation Considerations
- **Traffic flow**: Limit visible indicators to the closest two exhibits to prevent crowding and visual clutter.  
- **Aesthetic harmony**: Match icon colors, shapes, and glow intensity to the exhibit’s lighting and design language.  
- **Accessibility**: Offer high-contrast indicator variants, adjustable dwell durations, and alternative tap or voice command activation.  

--- -->

## Supplementary Information

### Biography
<!-- Developed by AR UX designer Thomas Lee for the “Digital Layers” initiative at the Modern Art Museum, 2024. -->

---

## Discussion
Key challenges include harmonizing indicator placement with exhibit aesthetics and ensuring voice/gesture activation works reliably across varied lighting and noise conditions. Future enhancements might personalize indicators based on visitor profiles or dynamically adjust glow intensity in crowded spaces.


## Media 


## Notes 
This pattern helps prevent missed opportunities for engagement by making AR content clearly discoverable and easily triggerable. It supports both first-time and returning visitors by offering consistent, recognizable AR interaction cues.
