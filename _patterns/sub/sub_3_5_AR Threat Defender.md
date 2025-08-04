---
layout: pattern
title: "Object Catching"
category: "sub-level"
pattern_category: presenter
order: 3.5

tags:
  - Environmental Awareness
  - Embodied Interaction
  - Gamified Learning
thumbnail: /images/Gif/CoralReef.gif
summary: "Defending Ecosystems through AR-Based Environmental Challenges"
description: "Transform invisible environmental threats into an interactive AR defense game, enabling visitors to protect vulnerable habitats through gestures while learning about real-world ecological impacts and solutions."
---
# Object Catching

---
## Overview
- **Name**  
  AR Object Catching
- **Intent**  
  Convey invisible or abstract environmental threats through interactive AR gameplay, fostering urgency and empathy while teaching mitigation strategies.

---

## Target
- **Problem**  
  Invisible or abstract threats—such as pollution or climate impacts—are difficult to convey in static exhibits, reducing visitor empathy and sense of agency.
- **Context**  
  - Natural-history or environmental exhibits illustrating hazards (ghost nets, acidic runoff)  
  - AR can render and animate non-physical threats in situ  
  - Installation supports real-time gestural tracking  
- **Use When**  
  - The exhibit aims to illustrate environmental hazards and empower visitors to act  
  - Visitors can interact gesturally (hand or body tracking)  
  - Threats are dynamic and benefit from active interception  
- **Forces**  
  - **Visibility vs. Realism**: Threats must look tangible without breaking immersion  
  - **Engagement vs. Complexity**: Gestures should be intuitive yet varied enough to teach concepts  
  - **Feedback Latency**: Real-time responses crucial to maintain sense of cause and effect  
  - **Emotional Impact**: Balancing urgency without overwhelming visitors  
- **Consequences**  
  - **Positive**: Deepens empathy, makes abstract hazards concrete, reinforces learning through action  
  - **Negative**: Poor tracking or slow feedback can frustrate; overly aggressive challenges may deter participation  

---

## Application

### Solution
1. **Gesture-Based Object Interception**  
   - Spawn virtual threats (drifting nets, plastic debris) moving toward vulnerable exhibit zones (e.g., coral reef).  
   - Track visitor hand/body gestures to block, deflect, or capture threats in mid-air.

2. **Targeted Protection & Progressive Challenges**  
   - Highlight critical zones when they’re at risk (glow or pulse).  
   - Increase difficulty over time: faster threats, multiple simultaneous objects, or visual obfuscation (murkiness).

3. **Start-Point Guidance with Animated Prompts**  
   - Begin with a short cinematic explaining real-world origin and impact of each threat.  
   - Display ghost-hand overlays or arrows showing the protective gesture required (e.g., sweeping motion).

4. **Narration & Real-Time Feedback**  
   - Play spatialized audio narrating impact stats when a threat is intercepted or missed.  
   - Show visual effects: healthy coral brightening and fish population bloom for successful defenses.

5. **Educational Wrap-Up**  
   - After the session, display personalized metrics (objects intercepted, reef health score).  
   - Present actionable conservation tips visitors can adopt outside the museum.

### Rationale
Turning abstract environmental hazards into tangible, interactive threats leverages embodied action to build empathy and reinforce learning; immediate feedback ties visitor effort directly to positive virtual outcomes.

### Design Parameters
- **Threat Speed**: Start at 0.5 m/s, increase by 0.1 m/s every 20 seconds  
- **Gesture Window**: Recognition window of 0.3–0.5 s for swipe or block motions  
- **Highlight Radius**: 0.5 m glow around at-risk zones  
- **Feedback Delay**: ≤ 0.1 s between gesture and visual/audio response  
- **Session Duration**: 60–120 s for optimal engagement  

### Game Mechanics
- **Score Meter**: Tracks number of threats intercepted  
- **Combo Bonus**: Extra points for consecutive successful blocks  
- **Lives System**: Allow 3 misses before “reef health” fails, prompting game over  
- **Unlockables**: New threat types or conservation tips unlocked based on performance  

### Related Pattern
<!-- - AR Exhibit Reassembler (interactive assembly)  
- Exhibit Knowledge Trigger (micro-task activation) -->

### Impact on Immersion
- **Enhances**: Makes invisible hazards visible and urgent; fosters active learning  
- **Risks**: Tracking failures or UX latency break presence; overly difficult stages can frustrate

### Example
<div class="intro-video-wrapper">
  <iframe
    src="https://www.youtube-nocookie.com/embed/3VmuF4z6loY"
    title="YouTube video player"
    frameborder="0"
    allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture"
    allowfullscreen
  ></iframe>
</div>
<!-- In a coral reef exhibit, plastic bottles drift toward a virtual reef. Visitors sweep their arms to deflect debris; each successful block triggers a coral-brightening animation and upbeat chime, while misses cause subtle reef graying and a soft alert tone. At the end, a summary screen shows intercepted debris count and suggests real-world recycling actions. -->

---
## Narrative Creation in Cultural Heritage

### Visitor Behavioral Goals
- **Build empathy**: Encourage visitors to feel responsible by intercepting virtual threats before they reach vulnerable exhibit zones.  
- **Learn mitigation**: Guide visitors to perform protective gestures that model real-world conservation actions.  

### AR Experience Indicators
- **Threat visuals**: Animated debris or nets with semitransparent textures that drift toward highlighted exhibit areas.  
- **Risk highlights**: Pulsing glow around endangered zones (e.g., coral reef) to signal where intervention is needed.  

### Interactive Narrative
1. **Audio cue**: A sharp “block” sound on successful interception and a low warning tone when a threat breaches the zone.  
2. **Visual cue**: Immediate particle burst and brightening of the protected area on success; brief darkening or desaturation on miss.  
3. **Narration launch**: A concise voiceover stating “You intercepted X pieces” or “Y threats got through,” paired with on-screen conservation tips.  

### Experience Principles
- **Intuitive gestures**: Use natural swipe or block motions—mirroring real cleanup actions—to minimize learning curve.  
- **Instant reinforcement**: Provide feedback within 0.1 s to tie visitor effort directly to virtual outcomes and sustain engagement.  
- **Balanced urgency**: Calibrate threat pacing so visitors feel motivated but not overwhelmed.  

### Curation Considerations
- **Gesture calibration**: Adjust recognition sensitivity per space and lighting to reduce false positives/negatives.  
- **Emotional tone**: Tune audio and visual feedback to maintain a hopeful, actionable mood rather than despair.  
- **Accessibility**: Offer alternate input options (e.g., button taps), captioned narration, and adjustable audio volumes.  



---

## Supplementary Information

### Biography
-

---

## Discussion
Key challenges include ensuring robust gesture recognition in varied lighting and space conditions, and balancing threat pacing to foster both engagement and educational impact. Future work could integrate cooperative multiplayer defense or dynamically tailor threat types based on visitor profiles.





## Notes

By turning hazard mitigation into an embodied game, this pattern converts abstract ecological data into visceral experience, driving home the importance—and attainability—of environmental stewardship.