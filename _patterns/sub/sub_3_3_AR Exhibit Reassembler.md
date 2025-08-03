---
layout: pattern
title: "Exhibit Reassembler"
category: "sub-level"
pattern_category: presenter
order: 3.3

tags:
  - Reconstruction
  - Interactive Learning
  - Hands-on Exploration
thumbnail: /images/Gif/Triceratops.gif
summary: "Reassembling Incomplete Exhibits through AR Interaction"
description: "Enable visitors to reconstruct missing parts of physical exhibits using AR-based jigsaw mechanics, enhancing structural understanding and engagement through guided, interactive assembly."
---

# AR Exhibit Reassembler

---
## Overview
- **Name**  
  AR Exhibit Reassembler  
- **Intent**  
  Enable visitors to virtually reconstruct missing artifact components through an interactive 3D puzzle, deepening comprehension of the whole form and its significance.

---
## Target
- **Problem**  
  When only partial physical artifacts are on display, visitors struggle to grasp the complete structure and relationships between parts.
- **Context**  
  - Exhibits with missing components (fossils, machinery, relics)  
  - Digital reconstructions available for the absent pieces  
  - Desire to engage users in an active, hands-on learning process  
- **Use When**  
  - Visitors encounter artifacts with substantial missing elements  
  - The goal is to teach overall structure via participatory assembly  
- **Forces**  
  - **Engagement vs. Complexity**: Balancing puzzle difficulty to avoid frustration  
  - **Accuracy vs. Playfulness**: Ensuring reconstructions are correct while remaining fun  
  - **Spatial Registration**: Aligning virtual pieces precisely with the physical artifact  
  - **Feedback Responsiveness**: Providing timely confirmation to sustain motivation  
- **Consequences**  
  - **Positive**: Active learning, improved spatial understanding, memorable interaction  
  - **Negative**: Poor tracking or misplacements can cause confusion; overly simple puzzles may feel trivial  

---
## Application

### Solution
1. **Jigsaw-Puzzle Mechanic**  
   - Spawn interactive 3D fragments representing the missing parts.  
   - Allow visitors to drag or gesture-match edges/textures to snap pieces into place on the physical artifact.  

2. **Progression Feedback**  
   - On correct placement, play a glow animation on the piece and an encouraging audio cue.  
   - Update a visible completion meter (e.g., “3 of 8 pieces assembled”).  

3. **Adaptive Challenge**  
   - Start with boundary or high-contrast pieces for early confidence.  
   - Introduce subtler shapes or mirrored fragments as users progress, adapting based on placement speed and errors.  

4. **Guidance & Tutorial**  
   - Highlight an initial docking region with a pulsing indicator.  
   - Play a brief voice-over or display on-screen instructions explaining controls and objectives.  

5. **Narrative Enhancements**  
   - As sections assemble, trigger contextual facts (e.g., “This vertebra supported the spinal cord”) via text and audio to weave learning into the flow.

### Rationale
Transforming passive viewing into active assembly engages spatial reasoning and contextualizes individual components within the artifact’s holistic form, reinforcing educational outcomes.

### Design Parameters
- **Piece Count**: 6–12 fragments to balance challenge and completion time  
- **Snap Tolerance**: 0.1–0.2 m positional threshold, 5–10° rotational allowance  
- **Feedback Delay**: ≤ 0.2 s between placement and confirmation  
- **Completion Meter**: Updated immediately upon each placement  
- **Tutorial Duration**: 5–8 s voice-over with visual highlights  

### Game Mechanics
- **Puzzle Badge**: Award “Master Reassembler” upon full assembly  
- **Speed Run**: Time from first pick to final snap for a leaderboard  
- **Hint Tokens**: Earn or purchase hints to highlight next piece or region  

### Related Pattern
- Exhibit Knowledge Trigger (focused micro-task)  
- Avatar Guide (guided pacing and narrative)

### Impact on Immersion
- **Enhances**: Hands-on engagement, spatial learning, narrative context  
- **Risks**: Tracking jitter or misalignment breaks presence; excessive tutorial can feel patronizing

### Example
<div class="intro-video-wrapper">
  <iframe
    src="https://www.youtube-nocookie.com/embed/pYIqsSc2lLg"
    title="YouTube video player"
    frameborder="0"
    allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture"
    allowfullscreen
  ></iframe>
</div>
<!-- In a dinosaur exhibit, visitors slide 3D femur and rib fragments into place on a partial skeleton. Each correctly snapped bone glows and plays a short roar, while a meter tracks progress. Upon completion, a voice-over narrates the full skeletal structure and its function. -->

---
## Narrative Creation in Cultural Heritage

### Visitor Behavioral Goals
- **Engage curiosity**: Invite visitors to explore missing fragments by displaying ghosted outlines of each piece and prompting “Tap to pick up.”  
- **Hands-on reconstruction**: Encourage active participation by letting visitors drag and snap virtual fragments into place at their own pace.  

### AR Experience Indicators
- **Ghost outlines**: Faint silhouettes of missing components appear over the physical artifact to indicate where pieces belong.  
- **Snap zone markers**: Pulsing rings or highlighted edges around target areas show valid placement regions.  

### Interactive Narrative
1. **Audio cue**: A soft “snap” sound plays when a fragment enters the correct zone, and a brief “pickup” tone on initial grab.  
2. **Visual cue**: The fragment glows and briefly pulses on correct placement; the completion meter increments with an animated fill.  
3. **Narration launch**: Contextual facts (“This rib supported the chest cavity”) auto-play and display as text once each fragment is secured.  

### Experience Principles
- **Intuitive interaction**: Use direct manipulation (grab, drag, release) paired with clear visual markers to guide assembly without menus.  
- **Immediate feedback**: Confirm actions within 0.2 s to maintain flow and reinforce learning through positive reinforcement.  
- **Self-paced discovery**: Allow visitors to pause, inspect, and resume assembly without time pressure or forced sequencing.  

### Curation Considerations
- **Spatial accuracy**: Calibrate snap tolerances (0.1–0.2 m, 5–10°) per exhibit to minimize frustration from misalignments.  
- **Aesthetic integration**: Match fragment shading and highlight styles to the artifact’s palette and exhibit lighting.  
- **Accessibility**: Offer alternative input (e.g., gesture-free selection), adjustable highlight contrast, and captions for audio narration.  



---
## Supplementary Information

### Biography
<!-- Designed by paleontology AR specialist Dr. Anika Vogel for the “Lost Giants” exhibit at the Natural History Forum, 2025. -->

---

## Discussion
Key challenges include ensuring robust spatial anchoring of virtual pieces and balancing puzzle difficulty. Future enhancements might introduce cooperative assembly for group learning or dynamically generate piece shapes based on user skill level.


## Notes

This pattern transforms incomplete physical remains into a hands-on, completion-driven experience that reinforces structural understanding and sustains visitor motivation.
