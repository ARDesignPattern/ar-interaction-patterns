---
layout: pattern
title: "Experience Presenter"
category: "high-level"
pattern_category: presenter
overlay: /images/PatternIcon/whale Tour.png
order: 3

tags:
  - Exploration
  - Experience Navigation
thumbnail: /images/high_presenter.png
summary: "Exploring and Controlling AR Content"
description: "Exploring and Controlling AR Content: Present the content in a structured, navigable, and user-controlled manner."
---
  <div class="column">
    <img src="{{ '/images/HomePage/Fig_ExperiencePresenter.png' | relative_url }}" alt="AR Interaction" class="profile">
  </div> 

# Experience Presenter
A modular AR system that structures exhibit content into self-paced, user-selectable segments.

---
## Overview
- **Name**  
 AR Experience Presenter
- **Intent**  
  Offer a modular, self-paced AR content delivery system that organizes complex exhibit information into manageable, user-selected segments.

---

## Target
- **Problem**  
  Visitors face information overload when an exhibit contains multiple thematic layers (eg.: historical, scientific, cultural) with no clear structure or control over pacing.
- **Context**  
  - Exhibits integrate rich, categorized AR overlays (3D models, text, audio)  
  - Visitors vary in prior knowledge and interests  
  - A flexible presentation improves engagement and comprehension  
- **Use When**  
  - Users have activated the AR experience for an exhibit  
  - Visitors wish to explore diverse content areas at their own speed  
  - The exhibit’s subject spans several dimensions or themes  
- **Forces**  
  - **Comprehensiveness vs. Cognitive Load**: Balancing depth of content with visitor attention spans  
  - **Control vs. Guidance**: Letting users choose their path while providing a coherent structure  
  - **Consistency vs. Variety**: Maintaining a uniform UI while supporting different content types  
- **Consequences**  
  - **Positive**: Empowers personalized exploration; reduces frustration; improves retention  
  - **Negative**: Too many modules may overwhelm; users might skip essential information  

---

## Application

### Solution (High-Level, Principle-Only)
1. **Purpose & Scope**  
Establish a **modular, self-paced** presentation convention that structures the journey **Discover → Select → Present → Deepen/Branch → Pause/Resume → Exit/Return**; define **principles and contracts**, not specific widgets, layouts, or timings.

2. **Invariants (must always hold)**
- **Discoverable without overload**
- **Pace controllable** (pause, resume, jump)
- **Progressive disclosure** (digestible units)
- **Redundant multimodality** (≥2 channels)
- **Consistent semantics** across exhibits

3. **Design Choices(Variation Points)** 
- Module organization: thematic groups, hierarchies, timelines, spatial partitions
- Unit granularity: micro to macro; adapt to engagement
- Navigation: sequential, free-jump, milestones, guided paths
- Modality mix: text, imagery/3D, narration/captions, micro-interactions
- Persistence: progress memory, bookmarks, context restore

4. **Decision Guidelines (Heuristics)**  
Choose granularity and navigation by prior knowledge, time budget, spatial density, device/localization confidence; reduce concurrent channels in noisy or crowded contexts.

5. **Integration Protocol (system-level agreement)**  
- Define states and events: **Users progress through the lifecycle: from seeing the content modules (thematic categories), selecting one, viewing its units, completing them, and finally finishing the module**
- Define exceptions and rollbacks: **Paused, Off-Focus, Low-Confidence, Overload**
- Expose telemetry hooks: **Enter/exit module, dwell time, jump/rollback, completion rate** 
- Avoid locking down UI details (like button shapes) or fixed timings (like unit length).

6. **Safety & Comfort Guards**
- Limit the amount of content per unit and the number of simultaneous media channels. Ensure all media can be paused or skipped, and that the system degrades smoothly if performance or tracking confidence drops.

7. **Accessibility & Inclusivity**
Offer equivalent paths (captions/transcripts, adjustable contrast/size, non-color encoding, voice/hands-free); provide concise summaries for reduced cognitive load.

### Rationale
- Focuses less on the **specific way of presenting** and more on **the core guarantees the system must provide** (e.g., pacing control, accessibility, consistent structure). freeing sub-pattern creativity.
- **Balances personalization and consistency** via invariants and equivalent access paths.
- **Manages cognitive load and pacing** with progressive disclosure and interruptible media.
- **Enables composition and extensibility** by treating interactive micro-tasks as modules within a stable contract.
- **Supports evidence-based iteration** with standardized states and telemetry for long-term governance.

<!-- ### Example -->
<!-- At a Roman artifact display, visitors tap the “Construction” tab to see animated building phases, then choose “Material Analysis” for microscopic texture overlays with narrated commentary, progressing at their own pace via Next/Previous controls. -->

---
<!-- ## Narrative Creation in Cultural Heritage

### Visitor Behavioral Goals
- **Draw visitors in**: Present a concise module overview popup on AR activation, showcasing thematic segments to pique interest.  
- **Auto-start interaction**: Automatically play the first available content module when the visitor enters the exhibit trigger area.  

### AR Experience Indicators
- **Narrative marking**: Subtle glowing border or shaded area around the exhibit base indicating interactive AR content zones.  
- **Guiding element**: Floating module icons/hand menu/tab buttons hovering near the exhibit that clearly denote selectable content segments.  

### Interactive Narrative
- **Narration design**: Short, scripted voiceovers that introduce each content segment, synchronized with on-screen captions and visuals. 
- **Audio cue**: Directly play related exhibit narration after the module selection.  
- **Visual cue**: Highlight the narration section in the exhibition, indicate the current narration category, and provide the completion rate/number of current narratives.
 

### Experience Principles
- **Intuitive guidance**: Use consistent iconography and spatial placement so visitors immediately recognize and select content modules.  
- **Seamless transition**: Visual and audio presentations should correspond with narration. Module transitions should maintain smooth animation connections to avoid abrupt jumps.
- **Comfortable pacing**: Let visitors control dwell time on each segment, offering clear “Next/Previous” controls; disabling auto-advance when needed. 

### Curation Considerations
- **Traffic flow**: Limit visible modules to the nearest two or three to reduce cognitive load and avoid crowd bottlenecks.  
- **Aesthetic harmony**: Match UI colors, fonts, and panel styles to the exhibit’s design language and lighting conditions.  
- **Accessibility**: Provide high-contrast UI themes, adjustable text sizes, and captioned audio for visitors with diverse needs.  
--- -->

## Supplementary Information

### Biography
<!-- Developed by AR curator Dr. Lena Hoffmann for the “Layers of Time” exhibition at the Historical Arts Center, 2025. -->

---

## Discussion
Key challenges include limiting module count to avoid choice paralysis and ensuring seamless transitions between media types. Future enhancements might include adaptive module suggestions based on visitor profile or integrating social sharing of completed modules.

## Media


## Notes
This pattern supports deep, self-directed learning by combining information structure with user navigation control. It works especially well for content-rich exhibits in cultural heritage, science, or educational AR environments.
