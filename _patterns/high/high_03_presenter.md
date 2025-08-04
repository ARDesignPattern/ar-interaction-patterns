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

# AR Experience Presenter
---
## Overview
- **Name**  
  AR Experience Presenter
- **Intent**  
  Offer a modular, self-paced AR content delivery system that organizes complex exhibit information into manageable, user-selected segments.

---

## Target
- **Problem**  
  Visitors face information overload when an exhibit contains multiple thematic layers (historical, scientific, cultural) with no clear structure or control over pacing.
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

### Solution
1. **Exhibit Information Categorization**  
   - Divide AR content into clear modules (e.g., “Anatomical Features,” “Habitat,” “Cultural History”).  
   - Present module buttons or tabs in a persistent menu.  
2. **Detailed Exhibit Explanation**  
   - Within each module, display one content item at a time—3D model animations, labeled overlays, or synced audio/subtitles.  
   - Highlight key elements visually and narrate explanations in short segments.  
3. **Navigation Controls**  
   - Provide “Previous” and “Next” buttons to move between items.  
   - Disable auto-advance; allow unlimited dwell time on each segment.  
4. **Category Indicators**  
   - Show the active module name prominently at the top of the view.  
   - Dim or collapse inactive modules to maintain focus.  
5. **Control for Animated Content**  
   - For videos or timed animations, include “Pause” and “Resume” controls.  
   - Auto-pause when navigating away; auto-resume upon return.

### Rationale
Structuring AR content into discrete, labeled modules reduces cognitive load, lets visitors prioritize their interests, and prevents information dumping by pacing delivery.

### Design Parameters
- **Modules per Exhibit**: 3–5 to balance depth and simplicity  
- **Button Size**: ≥ 50 px tap target  
- **Text Segment Length**: ≤ 40 words per panel  
- **Audio Clip Duration**: 10–20 s each  
- **Animation Control Latency**: ≤ 0.2 s for pause/resume  

<!-- ### Game Mechanics
- **Completion Badge**: Earn “Content Navigator” for viewing all modules  
- **Choice Path**: Unlock a “Deep Dive” quiz after completing core modules  
- **Time Tracker**: Show total time spent per module for playful feedback   -->

### Related Pattern
- Sequential Explanation (step-by-step panels)  
<!-- - AR Experience Indicator (discovering interactive exhibits)   -->

### Impact on Immersion
- **Enhances**: Provides clear mental model; supports autonomy and deeper learning  
- **Risks**: UI elements may occlude exhibits; overly linear flow could feel restrictive  

### Example
<!-- At a Roman artifact display, visitors tap the “Construction” tab to see animated building phases, then choose “Material Analysis” for microscopic texture overlays with narrated commentary, progressing at their own pace via Next/Previous controls. -->

---
## Narrative Creation in Cultural Heritage

### Visitor Behavioral Goals
- **Draw visitors in**: Present a concise module overview popup on AR activation, showcasing thematic segments to pique interest.  
- **Auto-start interaction**: Automatically highlight the first available content module when the visitor’s gaze fixes on the exhibit area.  

### AR Experience Indicators
- **Floor marking**: Subtle glowing border or shaded area around the exhibit base indicating interactive AR content zones.  
- **Guiding element**: Floating module icons or tab buttons hovering near the exhibit that clearly denote selectable content segments.  

### Interactive Narrative
1. **Audio cue**: A soft confirmation tone and brief voice prompt (“Module: Cultural History”) when a visitor selects a module.  
2. **Visual cue**: The activated module button pulses and the content panel smoothly slides into view.  
3. **Narration design**: Short, scripted voiceovers that introduce each content segment, synchronized with on-screen captions and visuals.  

### Experience Principles
- **Intuitive guidance**: Use consistent iconography and spatial placement so visitors immediately recognize and select content modules.  
- **Seamless transition**: Animate module panels in and out without abrupt cuts, maintaining visual flow as users navigate.  
- **Comfortable pacing**: Let visitors control dwell time on each segment, disabling auto-advance and offering clear “Next/Previous” controls.  

### Curation Considerations
- **Traffic flow**: Limit visible modules to the nearest two or three to reduce cognitive load and avoid crowd bottlenecks.  
- **Aesthetic harmony**: Match UI colors, fonts, and panel styles to the exhibit’s design language and lighting conditions.  
- **Accessibility**: Provide high-contrast UI themes, adjustable text sizes, and captioned audio for visitors with diverse needs.  


---

## Supplementary Information

### Biography
Developed by AR curator Dr. Lena Hoffmann for the “Layers of Time” exhibition at the Historical Arts Center, 2025.

---

## Discussion
Key challenges include limiting module count to avoid choice paralysis and ensuring seamless transitions between media types. Future enhancements might include adaptive module suggestions based on visitor profile or integrating social sharing of completed modules.

## Media


## Notes
This pattern supports deep, self-directed learning by combining information structure with user navigation control. It works especially well for content-rich exhibits in cultural heritage, science, or educational AR environments.
