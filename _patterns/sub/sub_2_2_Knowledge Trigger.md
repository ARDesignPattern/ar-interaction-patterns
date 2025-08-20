---
layout: pattern
title: "Knowledge Trigger"
category: "sub-level"
pattern_category: indicator
order: 2.2

tags:
  - Exploration
  - Knowledge Activation
thumbnail: /images/Gif/GrabFish-ezgif.com-video-to-gif-converter.gif
summary: "Triggering Deeper Understanding Through Action"
description: "Engage visitors in concise, meaningful interactions that activate core scientific or cultural knowledge embedded in AR exhibits."
---

  <div class="column">
    <img src="{{ '/images/Gif/GrabFish-ezgif.com-video-to-gif-converter.gif' | relative_url }}" alt="AR Interaction" class="profile">
  </div> 
  
# Exhibit Knowledge Trigger
A brief interaction that unlocks deeper AR content by highlighting a key concept.

---
## Overview
- **Name**  
  Exhibit Knowledge Trigger
- **Intent**  
  Surface a single high-value concept through a brief, goal-oriented interaction that unlocks deeper AR content.

---
## Target
- **Problem**  
  Visitors may perceive AR prompts as decorative and overlook core scientific or cultural insights, reducing the exhibit’s interpretive value.  
- **Context**  
  - Exhibits feature specific behavioural or functional phenomena (e.g., echolocation) that benefit from hands-on demonstration  
  - Spatial affordances allow auxiliary virtual objects within a few metres of the primary exhibit  
  - Visitors are open to light, one-step interactions rather than lengthy manipulations  
- **Use When**  
  - A single concept needs highlighting before revealing richer AR layers  
  - Playful, embodied tasks boost engagement and illustrate cause-and-effect  
  - Learning should be scaffolded, rewarding exploration with additional content  
- **Forces**  
  - **Engagement vs. Friction**: Task must be intuitive enough to invite participation without oversimplifying the concept  
  - **Focus vs. Distraction**: Interaction loop must foreground the knowledge nugget without pulling attention too far from the exhibit  
  - **Spatial Accuracy**: Object placement and drop-zone detection require precise localization  
  - **Feedback Multimodality**: Visual, audio, and optional haptic cues must align to confirm success  
- **Consequences**  
  - **Positive**: Deepens understanding of the key concept; scaffolds learning; motivates further exploration  
  - **Negative**: Misregistration or failed pickups can frustrate users; poorly tuned feedback may feel gimmicky  

---
## Application

### Solution (Use the Orca skeleten exhibit as the example)
1. **Spatial Object Placement**  
   - Position an auxiliary virtual object (e.g., a fish) 2–3 m from the life-size orca model.  
   - Render a subtle “grab here” indicator when visitors approach (Optional).  
2. **Knowledge-Centric Interaction Loop**  
   - Prompt the visitor (voice/UI) to grab the fish.  
   - On pickup, orca orients toward the fish and plays a sonar click sequence with pulsed cone waveform.  
3. **Completion & Knowledge Delivery**  
   - When the fish is placed into the orca’s mouth zone:  
     - Play confirmation chime; cease sonar animation.  
     - Start the exhibit presentation, such as displaying a multimedia panel summarizing echolocation (frequency range, tactics, ecology).  
     - Offer a “Discover More” button to unlock feeding-behaviour mini-scenes or anatomy overlays  (Optional).  
4. **Feedback Cues**  
   - **Visual**: Fish outline glows within the drop zone; orca eyes blink on success.  
   - **Auditory**: Escalating pings as fish nears mouth, resolved by a soft “capture” tone.  
   <!-- - **Haptic (optional)**: Controller vibration or glove pulse upon correct release. -->

### Rationale
A focused micro-task leverages embodied interaction to make an abstract concept tangible, priming visitors for deeper AR layers once the core insight is understood.

### Design Parameters
- **3D Orca mode**: Same position of the physical exhibit  
- **Grab Fish 3D mode**: 2–3 m from primary exhibit  
- **Drop-Zone Radius**: 0.5–0.8 m around orca’s mouth  
<!-- - **Sonar Pulse Rate**: 4–6 clicks per second, cone angle ~30°   -->
- **Chime Duration**: 0.3 s for quick confirmation  
- **Panel Fade-In**: 0.5 s transition  

<!-- ### Game Mechanics
- **Knowledge Badge**: Award “Echolocation Expert” on first completion  
- **Speed Challenge**: Time from pickup to placement for a playful leaderboard  
- **Layer Unlock**: Completing the micro-task reveals advanced AR modules   -->

### Related Pattern
- Floor Circle (proximity-triggered activation)  
<!-- - Avatar Guide (guided pacing and narrative) -->

### Impact on Immersion
- **Enhances**: Promotes active learning, strengthens concept retention, feels rewarding  
- **Risks**: Jittery tracking or missed pickups can break flow; excessive UI panels may distract

### Example
<div class="intro-video-wrapper">
  <iframe
    src="https://www.youtube-nocookie.com/embed/HBKIbfCrwZk"
    title="YouTube video player"
    frameborder="0"
    allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture"
    allowfullscreen
  ></iframe>
</div>
<!-- A visitor grabs a virtual fish floating beside the AR orca. As the fish nears the orca’s mouth, increasing sonar pings build anticipation; dropping the fish triggers a chime and reveals a concise panel on echolocation, with an option to explore feeding-behaviour scenes. -->

---
<!-- ## Narrative Creation in Cultural Heritage

### Visitor Behavioral Goals
- **Draw visitors in**: Prompt curiosity by highlighting a floating virtual fish beside the orca and inviting a “grab” interaction.  
- **Auto-start interaction**: A detailed presentation automatically starts when the user successfully feeds the fish to the orca.

### AR Experience Indicators
- **Object highlight**: Glowing outline around the fish signals it’s interactive.  
- **Drop-zone marker**: A pulsing ring at the orca’s mouth indicates where to place the fish.  

### Interactive Narrative
- **Narration Design**: The narrative content should be related to the exhibits themselves as well as the interaction itself, such as how Orcas use sonar to locate their prey. 
- **Audio cue**: Play progressive sonar sounds after picking up the fish, ending with a cue sound when the fish is placed correctly.   
- **Visual cue**: When fish approach, their outlines gradually become brighter; after successful feeding, visual feedback is provided, such as a pop-up window indicating successful feeding.  


### Experience Principles
- **Intuitive guidance**: Use direct, hands-on actions (grab & drop) to illustrate the concept without menus.  
- **Seamless transition**: Provide instant multimodal feedback (visual, audio, haptic) to maintain flow from task to learning.  
- **Comfortable pacing**: Allow visitors to interact at their own speed—no countdowns or time pressure unless opting into challenges.  

### Curation Considerations
- **Traffic flow**: Stagger interaction availability, or avoid multiple users operating simultaneously: multiple users occupying the delivery area at the same time causes interaction difficulties.  
- **Aesthetic harmony**: Match fish and UI overlays to the exhibit’s visual style and ambient lighting.  
- **Accessibility**: Offer captions for audio cues, and adjustable outline contrast for visibility.  
--- -->

## Supplementary Information
### Biography
<!-- Built by AR educator Dr. Elena García for the “Marine Minds” exhibit at the Ocean Discovery Center, 2024. -->

## Discussion
Key tuning involves aligning drop-zone sensitivity with tracking fidelity and balancing the brevity of the task against the richness of the follow-on content. Future extensions could adapt the experience for groups or integrate adaptive difficulty based on visitor age.




## Notes

The Exhibit Knowledge Trigger pattern blends discovery learning with purposeful motion, ensuring each interaction yields an immediate educational payoff. By coupling a single-step task to an iconic behavioural demonstration, it magnifies visitor curiosity and seamlessly channels them into deeper AR content pathways.
