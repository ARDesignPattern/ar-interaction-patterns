---
layout: pattern
title: "Sequential Explanation"
category: "sub-level"
pattern_category: presenter
order: 3.1

tags:
  - Exploration
  - Experience Navigation
thumbnail: /images/Gif/SequentialExploration.gif
summary: "Exploring and Controlling AR Content"
description: "Exploring and Controlling AR Content: Present the content in a structured, navigable, and user-controlled manner."
---


# Sequential Explanation


---
## Overview
- **Name**  
  Sequential Explanation  
- **Intent**  
  Present exhibit information in logical categories and let visitors explore at their own pace using clear navigation controls.

---
## Target
- **Problem**  
  Visitors struggle to understand multiple categories of information and may feel overwhelmed or miss key details without structured guidance.  
- **Context**  
  - Exhibits encompass multiple information categories or numerous data points  
  - AR feature already activated, ready to display digital content  
  - Visitors require a comfortable, self-paced exploration flow  
- **Use When**  
  - Visitors have engaged the exhibit’s AR information feature  
  - A comprehensive, tiered presentation of content is needed  
  - Users benefit from explicit controls to move between sections  
- **Forces**  
  - **Cognitive Load**: Balancing depth of content with visitor attention span  
  - **Pacing Control**: Allowing users to linger or skip ahead  
  - **Spatial Context**: Ensuring UI elements don’t obstruct the exhibit  
  - **Consistency**: Maintaining a uniform navigation model across categories  
- **Consequences**  
  - **Positive**: Clear mental model of content structure; users feel in control  
  - **Negative**: Overly linear flow may frustrate visitors seeking serendipitous discovery; UI elements may distract if poorly placed  

---
## Application

### Solution
1. **Exhibit Information Categorization**  
   - Break down all content into distinct categories (e.g., History, Function, Fun Facts).  
   - Display a set of buttons or tabs—one per category—at the top or side of the view.  
2. **Detailed Exhibit Explanation**  
   - Within each category, present information panels sequentially: images, text, 3D models, or video.  
   - Highlight key visual components (e.g., animate structural parts) and play aligned audio narration.  
3. **Navigation Controls**  
   - Provide “Previous” and “Next” buttons to move between panels.  
   - Optionally show a progress indicator or step count (e.g., “2 of 5”).  
4. **Category Indicators**  
   - Always display the active category title prominently.  
   - Dim or collapse inactive categories to maintain focus.  
5. **Control for Animated Content**  
   - For any looping animation or video, include “Pause” and “Resume” controls.  
   - Auto-pause when users navigate away, auto-resume if they return.

### Rationale
Structuring content into bite-sized, thematically grouped segments reduces overwhelm and gives visitors agency to explore at their own speed, improving comprehension and retention.

### Design Parameters
- **Categories**: 3–6 per exhibit to balance breadth and simplicity  
- **Button Size**: ≥ 40px height/tap target for easy selection  
- **Panel Duration**: Auto-advance disabled; allow unlimited reading time  
- **Progress Indicator**: Show step count (e.g., “Step 1/4”) or progress bar  
- **Animation Controls**: Pauses after 10 s of inactivity in a panel with moving content  

<!-- ### Game Mechanics
- **Completion Badge**: Award “Explorer” badge for visiting all panels in a category  
- **Quiz Unlock**: After finishing a category, unlock a short quiz mini-game  
- **Time Trial**: Track how quickly users cycle through panels for a playful challenge   -->

### Related Pattern
- Exhibit Knowledge Trigger (micro-task to surface key concept)  
<!-- - Floor Circle (proximity-based AR activation) -->

### Impact on Immersion
- **Enhances**: Gives a clear, predictable structure; supports deeper learning  
- **Risks**: UI chrome may draw focus away from the physical exhibit; linear flow could feel rigid

### Example
<div class="intro-video-wrapper">
  <iframe
    src="https://www.youtube-nocookie.com/embed/ukEJim45PAE"
    title="YouTube video player"
    frameborder="0"
    allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture"
    allowfullscreen
  ></iframe>
</div>
<!-- At a dinosaur fossil display, visitors tap the “Anatomy” button to see sequential panels: labeled bone parts animated in 3D, narrated audio explaining each. They then click “Next” to view “Habitat” images with pause controls for immersive video. -->

---
## Narrative Creation in Cultural Heritage

### Visitor Behavioral Goals
- **Clarify structure**: Help visitors grasp the exhibit’s thematic breakdown (e.g., History, Function, Fun Facts) at a glance.  
- **Self‐paced exploration**: Empower visitors to linger on or skip sections according to their interests and time.  

### AR Experience Indicators
- **Category tabs**: Persistent, color‐coded buttons (e.g., “History,” “Function,” “Fun Facts”) that highlight the active section.  
- **Progress marker**: A subtle step counter or progress bar showing “Panel 2 of 5” within each category.  

### Interactive Narrative
1. **Audio cue**: A soft “page‐turn” sound when navigating panels to reinforce the transition.  
2. **Visual cue**: The newly active tab briefly pulses or underlines when selected.  
3. **Narration launch**: The first line of audio narration auto‐plays on panel entry, with caption text fading in concurrently.  

### Experience Principles
- **Unobtrusive UI**: Place controls at screen edges or floor‐pinned so as not to obscure the physical exhibit.  
- **Consistent navigation**: Use uniform icons and button layouts across all categories to reduce learning time.  
- **Cognitive relief**: Disable auto‐advance; let visitors control pacing without feeling rushed.  

### Curation Considerations
- **Exhibit aesthetics**: Match button shapes, fonts, and accent colors to the exhibit’s design language.  
- **Accessibility**: Provide high‐contrast tab outlines, adjustable text size, and optional subtitles for audio.  
- **Hardware variance**: Ensure touch targets (≥ 40 px) and gesture zones are comfortable on both tablets and HMDs.  


---
## Supplementary Information

### Biography
<!-- Designed by AR educator Sara Müller for the “Deep Time” exhibition at the Natural History Museum, 2025. -->

---

## Discussion
Key considerations include balancing the number of categories versus visitor patience, and ensuring navigation controls remain intuitive across varying AR hardware (e.g., handheld tablet vs. head-mounted display). Future work could explore adaptive sequencing based on visitor interests or prior interactions.





## Notes

This pattern supports structured, self-directed exploration by guiding visitors through categorized exhibit information at their own pace, enhancing comprehension and engagement.
