---
layout: pattern
title: "Feature Drawing"
category: "sub-level"
pattern_category: presenter
order: 3.4

tags:
  - Creative Expression
  - Interpretive Interaction
  - Speculative Reconstruction
thumbnail: /images//Gif/DeinonychusDemo.gif
summary: "Drawing and Exploring Interpretive Features in AR"
description: "Enable visitors to creatively sketch hypothetical features—like feathers or textures—directly onto 3D models, supporting scientific dialogue and participatory interpretation through AR drawing tools."
---

# AR Exhibit Feature Drawing

---
## Overview
- **Name**  
  AR Exhibit Feature Drawing
- **Intent**  
  Invite visitors to co-create and explore speculative or contested exhibit details through freehand AR sketching and comparison with expert models.

---

## Target
- **Problem**  
  Static presentations of speculative or partially unknown exhibit features limit engagement and creative interpretation.
- **Context**  
  - Exhibits rely on hypotheses or evolving consensus (feather morphology, extinct coloration, reconstruction details)  
  - AR can overlay an interactive canvas directly on or around 3D models  
  - Visitors benefit from hands-on, creative engagement  
- **Use When**  
  - Scientific or historical details are hypothetical or debated  
  - The exhibit’s goal is to spark visitor contribution, debate, and interpretation  
- **Forces**  
  - **Openness vs. Accuracy**: Balancing creative freedom with scientific fidelity  
  - **Accessibility vs. Complexity**: Making drawing intuitive without overwhelming novices  
  - **Persistence vs. Ephemerality**: Deciding whether visitor sketches remain session-only or contribute to a shared gallery  
  - **Feedback Timeliness**: Providing real-time stroke feedback without latency  
- **Consequences**  
  - **Positive**: Deepens engagement, fosters ownership and discussion, makes science participatory  
  - **Negative**: Poor drawing controls can frustrate visitors; conflicting community sketches may confuse rather than clarify  

---

## Application

### Solution
1. **Freehand & Pinch-Gesture Drawing**  
   - Provide a spatial canvas around or directly on the 3D exhibit model.  
   - Enable mid-air strokes for sketching details (feathers, textures) and pinch gestures to adjust brush size or erase.  

2. **Feature Customization Toolkit**  
   - Offer adjustable brush size, opacity, and a scientific-theory–inspired palette.  
   - Include layering and undo/redo for refinement.  

3. **Start-Point Guidance & Prompt Zones**  
   - Highlight recommended areas (e.g., wing surfaces, crests) with subtle markers.  
   - Display a brief on-screen prompt explaining how to begin.  

4. **Feedback & Comparative Overlay**  
   - Show real-time visual feedback for stroke accuracy and depth placement.  
   - Provide a toggle to overlay expert or consensus reconstructions for side-by-side comparison.  

5. **Creative Interpretation Gallery**  
   - On completion, allow visitors to save their designs to a shared AR gallery.  
   - Cycle through community submissions on a virtual wall to encourage discussion.

### Rationale
Allowing visitors to actively sketch hypotheses turns passive observation into participatory science, making speculative details tangible and fostering deeper curiosity and debate.

### Design Parameters
- **Brush Sizes**: 1–10 cm virtual width, adjustable via pinch span  
- **Opacity Levels**: 20–100% in 10% increments  
- **Stroke Latency**: ≤ 50 ms for real-time feel  
- **Prompt Zone Highlight**: 0.2 m radius pulsing halo  
- **Gallery Slot Limit**: Store up to 20 recent designs per exhibit  

### Game Mechanics
- **Community Badge**: Earn “Citizen Illustrator” for contributing a design  
- **Challenge Mode**: Attempt to match an expert sketch under a time limit  
- **Voting System**: Visitors can upvote favorite community sketches  

### Related Pattern
- Exhibit Knowledge Trigger (micro-task activation)  
- Floor Circle (proximity-based AR entry)

### Impact on Immersion
- **Enhances**: Transforms speculation into tangible interaction; fosters social learning  
- **Risks**: UI clutter if toolkit is too large; sketch overlays may obscure the physical artifact  

### Example
<div class="intro-video-wrapper">
  <iframe
    src="https://www.youtube-nocookie.com/embed/UrQMUq3n9PA"
    title="YouTube video player"
    frameborder="0"
    allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture"
    allowfullscreen
  ></iframe>
</div>
<!-- At a paleontology exhibit, visitors sketch feather patterns on a velociraptor model. They adjust brush thickness with pinches, compare their designs to a paleontologist’s rendition, and then submit their own version to the exhibit’s AR gallery wall. -->

---
## Narrative Creation in Cultural Heritage

### Visitor Behavioral Goals
- **Spark creativity**: Encourage visitors to imagine and sketch speculative features (e.g., feather patterns) directly on the exhibit model.  
- **Compare perspectives**: Invite side-by-side exploration of personal sketches and expert reconstructions to foster critical thinking.  

### AR Experience Indicators
- **Prompt zones**: Subtle pulsing halos around recommended drawing areas (e.g., wings, crests) guide where to begin.  
- **Tool icons**: Floating brush and eraser icons that appear when users perform pinch gestures to select tools.  

### Interactive Narrative
1. **Audio cue**: A soft brush stroke sound when drawing begins and an erase “swoosh” on pinch-delete.  
2. **Visual cue**: Real-time stroke feedback with immediate line rendering and brush-size halo adjustments.  
3. **Comparison overlay**: A semi-transparent expert sketch fades in when the user toggles the “Expert View” button.  

### Experience Principles
- **Direct manipulation**: Let visitors draw mid-air strokes that adhere to the 3D model’s surface, avoiding separate menus.  
- **Fluid transitions**: Ensure seamless toggling between freehand and comparison modes without interrupting the creative flow.  
- **Creative freedom within bounds**: Provide guidelines via prompt zones but allow unrestricted sketching elsewhere.  

### Curation Considerations
- **Interface minimalism**: Keep brush controls unobtrusive—hide tool icons when idle to preserve focus on the artifact.  
- **Gallery management**: Limit saved designs to a recent curated set (e.g., 20 per exhibit) to maintain quality.  
- **Accessibility**: Offer adjustable stroke contrast, voice commands for tool selection, and subtitle prompts for all instructions.  


---

## Supplementary Information

### Biography
-

---

## Discussion
Critical tuning involves ensuring drawing controls are intuitive across devices and balancing community contributions so the shared gallery remains inspiring rather than chaotic. Future enhancements might include AI-assisted sketch suggestions or collaborative multi-user drawing sessions.


## Notes

This pattern elevates visitors from passive observers to active co-interpreters, fostering dialogue around uncertain scientific narratives and nurturing creative thinking.