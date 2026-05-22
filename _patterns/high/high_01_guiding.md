---
layout: pattern
title: "Point of Interest Guide"
category: "high-level"
pattern_category: guiding
pattern_group: poi-guide
overlay: /images/PatternIcon/Path.png
order: 1

tags:
  - PoI Guide
  - Route Guidance
  - Experience Navigation
thumbnail: /images/high_guide.png
summary: "Supporting visitor movement toward points of interest"
description: "The PoI Guide category organizes HMD-AR guidance patterns that help visitors locate, approach, and arrive at points of interest through spatial guidance, route support, pace regulation, and recoverable arrival logic."
---

<div class="column">
  <img src="{{ '/images/HomePage/Fig_POIGuide.png' | relative_url }}" alt="Point of Interest Guide" class="profile">
</div> 
  
# Point of Interest Guide

A category-level pattern class for guiding visitors toward points of interest in HMD-based AR museum experiences.

---

## Name

PoI Guide / Point of Interest Guide

---

## Level and Category

Category-level pattern class in the consolidated pattern system.

It groups guidance-related application-level patterns that support visitor movement toward points of interest in HMD-based AR museum experiences.

---

## Intent

Help visitors locate, approach, and arrive at selected points of interest in complex AR-enhanced exhibition spaces through spatial guidance, route support, pacing support, and multimodal feedback.

The category provides a system-level guidance structure that can be instantiated through different application-level patterns, such as **Avatar Guide** or **Forward Cue-Routing**.

---

## Rationale

Guidance in HMD-based AR museums is not only a matter of showing a destination. Visitors move through real exhibition spaces while attending to physical exhibits, other visitors, spatial obstacles, and digital overlays.

The PoI Guide class separates the general guidance function from its concrete representation. This allows creators to preserve a consistent guidance logic across an exhibition while choosing different guidance strategies according to route complexity, spatial layout, crowding, visitor intent, device capability, and desired narrative framing.

As a category-level class, PoI Guide defines the shared interaction role, variation dimensions, state logic, and composition position of guidance patterns without prescribing a single visual form, distance threshold, or interaction technique.

---

## Problem

Visitors in AR-enhanced museum or exhibition environments may miss important points of interest because exhibits are spatially dispersed, only partly visible, insufficiently supported by physical signage, or difficult to locate through conventional maps.

In HMD-based AR, this problem is intensified by limited field of view, divided attention, unfamiliar spatial cues, and the need to remain aware of other visitors and the physical environment while moving.

A reusable guidance structure is needed so that different guidance representations can support movement, orientation, pacing, route recovery, and arrival confirmation in a consistent way.

---

## Context

This category applies to standing and walking HMD-based AR museum experiences in which visitors move between points of interest before entering an exhibit-related AR experience. It is especially relevant when:

- multiple points of interest are distributed across an exhibition area;
- visitors need help locating the next exhibit or AR-enabled station;
- the route includes corridors, turns, junctions, open halls, or visually dense spaces;
- guidance must remain legible while preserving attention to exhibits and public-space safety;
- the experience needs to hand over from movement to activation and presentation patterns.

The category assumes that route geometry, point-of-interest metadata, safe viewing positions, and localization confidence can be represented sufficiently for guidance and arrival detection.

---

## Use When

Use this category when:

- visitors need to move from one point of interest to another;
- a museum experience requires a repeatable guidance phase before exhibit activation;
- creators need to choose between different guidance strategies, such as avatar-based guidance or ground-based cue routing;
- guidance needs to support route selection, turn anticipation, arrival confirmation, and recovery from deviation;
- the exhibition requires a consistent guidance logic across different exhibits while allowing local adaptation.

Avoid relying on this category as a separate interaction phase when the exhibit is immediately visible, when no route or movement support is needed, or when guidance cues would create safety risks, visual clutter, or excessive control over visitors’ free exploration.

---

## Forces

- **Efficiency vs. exploration:** Guidance should help visitors find intended points of interest, but should not remove opportunities for voluntary exploration and serendipitous discovery.
- **Clarity vs. clutter:** Guidance cues must be visible enough to support orientation, but not so persistent or dense that they overwhelm the HMD view.
- **Control vs. automation:** Visitors may benefit from automatic route support, but should still be able to pause, resume, change destination, or leave the guided route.
- **Guidance strength vs. exhibit attention:** Strong guidance can improve orientation, but may draw attention away from physical exhibits and the surrounding museum environment.
- **Pacing vs. comfort:** The route should support comfortable movement and avoid encouraging visitors to walk too quickly, turn sharply, or ignore obstacles.
- **Consistency vs. local adaptation:** Guidance semantics should remain recognizable across an exhibition, while cue form, modality, and intensity may adapt to local spatial conditions.
- **Multimodal redundancy vs. overload:** Visual, auditory, and other feedback channels can reinforce orientation, but excessive simultaneous cues may become distracting.
- **Spatial precision vs. recoverability:** Guidance should be spatially meaningful, but must degrade gracefully when tracking confidence, route alignment, or visitor position becomes uncertain.

---

## Solution

Define a system-level guidance structure that supports the visitor journey from point-of-interest selection to route preview, route commitment, navigation, turn anticipation, arrival, dwell, and continuation or exit.

The guidance layer should provide continuous orientation without over-specifying one particular representation. It may be implemented through a virtual guide, floor-based route cues, forward-facing indicators, audio prompts, haptic cues, or hybrid forms.

The category should preserve several invariants:

- guidance cues should be perceptible without occluding exhibits;
- movement support should remain pace-safe and comfortable;
- visitors should receive continuous orientation and recovery options when they pause, deviate, or lose the route;
- at least two feedback channels, such as visual and auditory feedback, should be available where possible;
- guidance-state meanings should remain consistent across exhibits, even when the concrete representation changes.

The category also defines a shared state logic. A typical route sequence includes:

**Select → Preview → Commit → Navigate → Anticipate Turn → Turn → Arrive → Dwell → Resume / End**

Exception states may include:

**Off Route → Paused → Low Tracking Confidence → Recovery**

Concrete application-level patterns should instantiate this logic through their own visual form, feedback style, pacing policy, and implementation parameters.

---

## Design Parameters and Recommended Settings

- **Guidance modality family:** Select between avatar-based guidance, ground-based cues, forward-facing overlays, audio prompts, haptic cues, or hybrid combinations. Use **Avatar Guide** when a social, narrative, or pace-regulated guide is desirable; use **Forward Cue-Routing** when lightweight and unobtrusive route indication is preferred.
- **Routing policy:** Define whether the route prioritizes shortest distance, smoothest movement, thematic order, accessibility, crowd avoidance, or curatorial narrative sequence.
- **Pacing policy:** Decide whether guidance behaves as a leader, follower, fixed-rhythm cue, adaptive route assistant, or user-paced route display.
- **Anticipation horizon:** Specify how early turns, junctions, or decision points should be announced. Increase anticipation in complex layouts and reduce it in short or narrow route segments.
- **Persistence and visibility:** Decide whether cues are always visible, shown on demand, shown only near decision points, or faded when the visitor is confidently following the route.
- **Destination selection:** Define whether destinations are selected by visitor choice, curatorial sequence, system recommendation, time constraint, or previously visited/unvisited status.
- **Feedback channels:** Combine visual guidance with optional spatial audio, captioned prompts, vibration where available, or other redundant cues. Avoid relying on a single channel when environmental conditions are uncertain.
- **Recovery behaviour:** Define what happens when the visitor deviates, pauses, walks in the wrong direction, or tracking confidence becomes low. Recovery should be calm, reversible, and easy to understand.
- **Arrival definition:** Define what counts as arrival, such as entering a radius around the point of interest, reaching a safe viewing position, or stopping within a predefined activation zone.
- **Accessibility settings:** Support adjustable cue size, brightness, contrast, text size, audio volume, pacing tempo, and non-colour-dependent cue semantics where possible.
- **Telemetry hooks:** Record route start, cue display, deviation, pause, recovery, arrival, and route completion events to support evaluation and debugging.

---

## Consequences

When applied successfully, the PoI Guide category can reduce spatial confusion, improve coverage of intended exhibition content, and support smoother transitions between movement and exhibit engagement. It can also make route guidance more reusable because different guidance representations can share a common state logic, event structure, and composition position.

However, the category also introduces risks. Overly directive guidance may reduce visitor autonomy and suppress exploratory museum behaviour. Persistent route cues may visually clutter the exhibition or distract from physical exhibits. If routing, arrival detection, or recovery behaviour is unreliable, visitors may lose trust in the AR system.

The category therefore requires careful balancing of guidance strength, cue visibility, routing policy, pacing, feedback redundancy, and recovery design.

---

## Related Patterns

- **Application-level patterns in this category**
  - **Avatar Guide** instantiates this category through a visible virtual guide or character that visitors can follow toward a point of interest.
  - **Forward Cue-Routing** instantiates this category through ground-based or forward-path cues that indicate direction, turns, and arrival.

- **Follow-up activation patterns**
  - **Step-In Trigger** commonly follows PoI guidance by indicating and activating the AR experience once visitors reach the point of interest.
  - **Exhibit Knowledge Trigger** commonly follows PoI guidance when activation should be tied to a short exhibit-related or concept-linked interaction.

- **Follow-up presentation patterns**
  - **Sequential Explanation** may follow guidance and activation when visitors need structured exhibit-related content.
  - **AR Labelling** may follow guidance and activation when visitors need spatially anchored labels or component-level explanations.
  - **AR Exhibit Reassembler** may follow guidance and activation when visitors should reconstruct missing or fragmented exhibit components.
  - **AR Exhibit Feature Drawing** may follow guidance and activation when visitors should draw, trace, or mark interpretive exhibit features.
  - **AR Object Catching** may follow guidance and activation when visitors should respond to virtual threats or objects around an exhibit.

---

## Composition Notes

PoI Guide normally occupies the first phase of a museum HMD-AR interaction sequence. It supports movement toward the point of interest and prepares the transition into indication, activation, and presentation.

A typical composition is:

**PoI Guide → Experience Indicator → Experience Presenter**

For example:

**Avatar Guide → Step-In Trigger → Sequential Explanation → AR Labelling**

or:

**Forward Cue-Routing → Exhibit Knowledge Trigger → AR Object Catching**

The handoff from guidance to activation should be explicit. When visitors arrive at the point of interest, the guidance cue should reduce intensity, stop, or transform into an arrival confirmation. The activation pattern should then become visually primary. This prevents visitors from confusing route following with exhibit interaction.

In multi-exhibit routes, the PoI Guide category can be repeated between points of interest, but each segment should have a clear start, route state, arrival state, and recovery behaviour.

---

## Implementation Alignment

As a category-level pattern, PoI Guide should be implemented as a shared route-orchestration layer rather than as a single visual prefab. This layer can coordinate destination selection, waypoint data, route preview, guidance-state transitions, cue visibility, visitor-distance monitoring, turn anticipation, arrival detection, recovery behaviour, and handoff events.

Application-level prefabs such as **Avatar Guide** and **Forward Cue-Routing** can then subscribe to the same route state and event structure while rendering different guidance representations.

Relevant implementation data include:

- point-of-interest metadata;
- route geometry;
- waypoint lists;
- safe viewing positions;
- arrival radii;
- localization-confidence values;
- cue-state definitions;
- route-state definitions;
- feedback-channel settings;
- telemetry hooks.

Implementation-level events may include:

- destination selected;
- route preview shown;
- route committed;
- guidance started;
- cue displayed;
- turn anticipated;
- waypoint reached;
- visitor deviated;
- guidance paused;
- recovery started;
- tracking confidence low;
- arrival confirmed;
- handoff triggered;
- route completed;
- guidance ended.

These events can support debugging, system logs, observation sheets, and later evaluation of route completion, deviation frequency, missed cues, recovery success, arrival recognition, and transition success.

---

## Example Use

In a natural-history museum, a visitor begins an HMD-AR experience and selects a whale skeleton as the next point of interest. The PoI Guide layer defines the route, previews the destination, and starts the guidance phase. Depending on the exhibition concept, this guidance may be instantiated as an **Avatar Guide** that visitors follow through the hall, or as **Forward Cue-Routing** that uses subtle floor-based ripples and directional sound cues.

As the visitor approaches the target area, the guidance state changes from navigation to arrival. The guide stops or the final route cue converges into an arrival marker. The guidance layer then hands over to an **Experience Indicator**, such as **Step-In Trigger** or **Exhibit Knowledge Trigger**, which activates the exhibit-related AR experience. After activation, the system continues into an **Experience Presenter** pattern, such as **Sequential Explanation** or **AR Labelling**.