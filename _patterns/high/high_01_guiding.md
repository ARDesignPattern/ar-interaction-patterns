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

<div class="ag-pattern" markdown="1">

<div class="ag-hero" markdown="1">

<p class="ag-eyebrow">CATEGORY-LEVEL PATTERN · POINT OF INTEREST GUIDE</p>

# Point of Interest Guide

<p class="ag-lead">
A category-level pattern class for guiding visitors toward
points of interest in HMD-based AR museum experiences.
</p>

<div class="ag-tags">
  <span>PoI Guide</span>
  <span>Route Guidance</span>
  <span>Experience Navigation</span>
  <span>Category-Level</span>
</div>

<div class="ag-hero-image">
  <img
    src="{{ '/images/HomePage/Fig_POIGuide.png' | relative_url }}"
    alt="Point of Interest Guide category illustration">
</div>

</div>

<div class="ag-section" markdown="1">

<p class="ag-section-number">01 / PATTERN DEFINITION</p>

## Pattern Identity

<div class="ag-metadata">
  <div>
    <span class="ag-meta-label">Name</span>
    <strong>PoI Guide / Point of Interest Guide</strong>
  </div>
  <div>
    <span class="ag-meta-label">Level</span>
    <strong>Category-Level Pattern</strong>
  </div>
  <div>
    <span class="ag-meta-label">Category</span>
    <strong>Guidance</strong>
  </div>
</div>

Category-level pattern class in the consolidated pattern system.

It groups guidance-related application-level patterns that support visitor movement toward points of interest in HMD-based AR museum experiences.

### Intent

Help visitors locate, approach, and arrive at selected points of interest in complex AR-enhanced exhibition spaces through spatial guidance, route support, pacing support, and multimodal feedback.

The category provides a system-level guidance structure that can be instantiated through different application-level patterns, such as **Avatar Guide** or **Forward Cue-Routing**.

</div>

<div class="ag-section" markdown="1">

<p class="ag-section-number">02 / DESIGN CHALLENGE</p>

## Problem and Rationale

<div class="ag-highlight-block" markdown="1">

### Problem

Visitors in AR-enhanced museum or exhibition environments may miss important points of interest because exhibits are distributed across the space, only partly visible, insufficiently supported by physical guidance, or difficult to locate through conventional maps.

In HMD-based AR, this problem is intensified by limited field of view, divided attention, unfamiliar spatial cues, and the need to remain aware of other visitors and the physical environment while moving.

A reusable guidance structure is needed so that different guidance representations can support movement, orientation, pacing, route recovery, and arrival confirmation in a consistent way.

</div>

### Rationale

Guidance in HMD-based AR museums is not only a matter of showing a destination. Visitors move through real exhibition spaces while attending to physical exhibits, other visitors, spatial obstacles, and digital overlays.

The PoI Guide class separates the general guidance function from its concrete representation. This allows creators to preserve a consistent guidance logic across an exhibition while choosing different guidance strategies according to route complexity, spatial layout, crowding, visitor intent, device capability, and desired narrative framing.

As a category-level class, PoI Guide defines the shared interaction role, variation dimensions, state logic, and composition position of guidance patterns without requiring a single visual form, distance threshold, or interaction technique.

</div>

<div class="ag-section" markdown="1">

<p class="ag-section-number">03 / APPLICABILITY</p>

## Context

This category applies to standing and walking HMD-based AR museum experiences in which visitors move between points of interest before entering an exhibit-related AR experience. It is especially relevant when:

- multiple points of interest are distributed across an exhibition area;
- visitors need help locating the next exhibit or AR-enabled station;
- the route includes corridors, turns, junctions, open halls, or visually dense spaces;
- guidance must remain legible while preserving attention to exhibits and public-space safety;
- the experience needs to hand over from movement to activation and presentation patterns.

The category assumes that route geometry, point-of-interest metadata, safe viewing positions, and localization confidence can be represented sufficiently for guidance and arrival detection.

### Use When

Use this category when:

- visitors need to move from one point of interest to another;
- a museum experience requires a repeatable guidance phase before exhibit activation;
- creators need to choose between different guidance strategies, such as avatar-based guidance or ground-based cue routing;
- guidance needs to support route selection, turn anticipation, arrival confirmation, and recovery from deviation;
- the exhibition requires a consistent guidance logic across different exhibits while allowing local adaptation.

<div class="ag-caution" markdown="1">

**Avoid When**

Avoid relying on this category as a separate interaction phase when the exhibit is immediately visible, when no route or movement support is needed, or when guidance cues would create safety risks, visual clutter, or excessive control over visitors’ free exploration.

</div>

</div>

<div class="ag-section" markdown="1">

<p class="ag-section-number">04 / DESIGN TRADE-OFFS</p>

## Forces

<div class="ag-forces" markdown="1">

### Efficiency vs. exploration

Guidance should help visitors find intended points of interest, but should not remove opportunities for voluntary exploration and serendipitous discovery.

### Clarity vs. clutter

Guidance cues must be visible enough to support orientation, but not so persistent or dense that they overwhelm the HMD view.

### Control vs. automation

Visitors may benefit from automatic route support, but should still be able to pause, resume, change destination, or leave the guided route.

### Guidance strength vs. exhibit attention

Strong guidance can improve orientation, but may draw attention away from physical exhibits and the surrounding museum environment.

### Pacing vs. comfort

The route should support comfortable movement and avoid encouraging visitors to walk too quickly, turn sharply, or ignore obstacles.

### Consistency vs. local adaptation

Guidance semantics should remain recognizable across an exhibition, while cue form, modality, and intensity may adapt to local spatial conditions.

### Multimodal redundancy vs. overload

Visual, auditory, and other feedback channels can support orientation, but excessive simultaneous cues may become distracting.

### Spatial precision vs. recoverability

Guidance should be spatially meaningful, but must recover smoothly when tracking confidence, route alignment, or visitor position becomes uncertain.

</div>

</div>

<div class="ag-section" markdown="1">

<p class="ag-section-number">05 / DESIGN RESPONSE</p>

## Solution

<div class="ag-solution" markdown="1">

Define a system-level guidance structure that supports the visitor journey from point-of-interest selection to route preview, route commitment, navigation, turn anticipation, arrival, dwell, and continuation or exit.

The guidance layer should provide continuous orientation without over-specifying one particular representation. It may be implemented through a virtual guide, floor-based route cues, forward-facing indicators, audio prompts, body-based cues, or hybrid forms.

### Guidance Invariants

The category should preserve several invariants:

- guidance cues should be perceptible without occluding exhibits;
- movement support should remain pace-safe and comfortable;
- visitors should receive continuous orientation and recovery options when they pause, deviate, or lose the route;
- at least two feedback channels, such as visual and auditory feedback, should be available where possible;
- guidance-state meanings should remain consistent across exhibits, even when the concrete representation changes.

### Shared State Logic

The category also defines a shared state logic. A typical route sequence includes:

<div class="ag-composition">
  <span>Select</span>
  <b>→</b>
  <span>Preview</span>
  <b>→</b>
  <span>Commit</span>
  <b>→</b>
  <span>Navigate</span>
  <b>→</b>
  <span>Anticipate Turn</span>
  <b>→</b>
  <span>Turn</span>
  <b>→</b>
  <span>Arrive</span>
  <b>→</b>
  <span>Dwell</span>
  <b>→</b>
  <span>Resume / End</span>
</div>

Exception states may include:

<div class="ag-composition">
  <span>Off Route</span>
  <b>→</b>
  <span>Paused</span>
  <b>→</b>
  <span>Low Tracking Confidence</span>
  <b>→</b>
  <span>Recovery</span>
</div>

Concrete application-level patterns should instantiate this logic through their own visual form, feedback style, pacing policy, and implementation parameters.

</div>

</div>

<div class="ag-section" markdown="1">

<p class="ag-section-number">06 / CONFIGURATION</p>

## Design Parameters and Recommended Settings

<div class="ag-param-highlights">

  <div class="ag-param-card">
    <strong>Modality</strong>
    <span>Guidance Representation</span>
    <small>Avatar, floor cues, audio, haptics, hybrid</small>
  </div>

  <div class="ag-param-card">
    <strong>Routing</strong>
    <span>Route and Pacing Policy</span>
    <small>Visitor, spatial, and curatorial priorities</small>
  </div>

  <div class="ag-param-card">
    <strong>Recovery</strong>
    <span>Guidance Continuity</span>
    <small>Pause, deviation, tracking and arrival</small>
  </div>

</div>

<div class="ag-table-scroll">
  <table>
    <thead>
      <tr>
        <th>Parameter</th>
        <th>Recommended Setting</th>
      </tr>
    </thead>
    <tbody>

      <tr>
        <td>Guidance modality family</td>
        <td>Select between avatar-based guidance, ground-based cues, forward-facing overlays, audio prompts, haptic cues, or hybrid combinations. Use <strong>Avatar Guide</strong> when a social, narrative, or pace-regulated guide is desirable; use <strong>Forward Cue-Routing</strong> when lightweight and subtle route indication is preferred.</td>
      </tr>

      <tr>
        <td>Routing policy</td>
        <td>Define whether the route prioritizes shortest distance, smoothest movement, thematic order, accessibility, crowd avoidance, or curatorial narrative sequence.</td>
      </tr>

      <tr>
        <td>Pacing policy</td>
        <td>Decide whether guidance behaves as a leader, follower, fixed-rhythm cue, adaptive route assistant, or user-paced route display.</td>
      </tr>

      <tr>
        <td>Anticipation horizon</td>
        <td>Specify how early turns, junctions, or decision points should be announced. Increase anticipation in complex layouts and reduce it in short or narrow route segments.</td>
      </tr>

      <tr>
        <td>Persistence and visibility</td>
        <td>Decide whether cues are always visible, shown on demand, shown only near decision points, or faded when the visitor is confidently following the route.</td>
      </tr>

      <tr>
        <td>Destination selection</td>
        <td>Define whether destinations are selected by visitor choice, curatorial sequence, system recommendation, time constraint, or previously visited/unvisited status.</td>
      </tr>

      <tr>
        <td>Feedback channels</td>
        <td>Combine visual guidance with optional spatial audio, captioned prompts, vibration where available, or other redundant cues. Avoid relying on a single channel when environmental conditions are uncertain.</td>
      </tr>

      <tr>
        <td>Recovery behaviour</td>
        <td>Define what happens when the visitor deviates, pauses, walks in the wrong direction, or tracking confidence becomes low. Recovery should be calm, reversible, and easy to understand.</td>
      </tr>

      <tr>
        <td>Arrival definition</td>
        <td>Define what counts as arrival, such as entering a radius around the point of interest, reaching a safe viewing position, or stopping within a predefined activation zone.</td>
      </tr>

      <tr>
        <td>Accessibility settings</td>
        <td>Support adjustable cue size, brightness, contrast, text size, audio volume, pacing tempo, and non-colour-dependent cue semantics where possible.</td>
      </tr>

      <tr>
        <td>Logging points</td>
        <td>Record route start, cue display, deviation, pause, recovery, arrival, and route completion events to support evaluation and debugging.</td>
      </tr>

    </tbody>

  </table>
</div>

</div>

<div class="ag-section" markdown="1">

<p class="ag-section-number">07 / DESIGN IMPLICATIONS</p>

## Consequences

<div class="ag-consequences" markdown="1">

### Benefits

When applied successfully, the PoI Guide category can reduce spatial confusion, improve coverage of intended exhibition content, and support smoother transitions between movement and exhibit engagement. It can also make route guidance more reusable because different guidance representations can share a common state logic, event structure, and composition position.

### Risks and Limitations

However, the category also introduces risks. Overly directive guidance may reduce visitor autonomy and suppress exploratory museum behaviour. Persistent route cues may visually clutter the exhibition or distract from physical exhibits. If routing, arrival detection, or recovery behaviour is unreliable, visitors may lose trust in the AR system.

The category therefore requires careful balancing of guidance strength, cue visibility, routing policy, pacing, feedback redundancy, and recovery design.

</div>

</div>

<div class="ag-section" markdown="1">

<p class="ag-section-number">08 / PATTERN LANGUAGE</p>

## Related Patterns

<div class="ag-related" markdown="1">

### Application-Level Patterns in This Category

**Avatar Guide** instantiates this category through a visible virtual guide or character that visitors can follow toward a point of interest.

**Forward Cue-Routing** instantiates this category through ground-based or forward-path cues that indicate direction, turns, and arrival.

### Follow-up Activation Patterns

**Step-In Trigger** commonly follows PoI guidance by indicating and activating the AR experience once visitors reach the point of interest.

**Exhibit Knowledge Trigger** commonly follows PoI guidance when activation should be tied to a short exhibit-related or concept-linked interaction.

### Follow-up Presentation Patterns

**Sequential Explanation** may follow guidance and activation when visitors need structured exhibit-related content.

**AR Labelling** may follow guidance and activation when visitors need spatially anchored labels or component-level explanations.

**AR Exhibit Reassembler** may follow guidance and activation when visitors should reconstruct missing or fragmented exhibit components.

**AR Exhibit Feature Drawing** may follow guidance and activation when visitors should draw, trace, or mark interpretive exhibit features.

**AR Object Catching** may follow guidance and activation when visitors should respond to virtual threats or objects around an exhibit.

</div>

</div>

<div class="ag-section" markdown="1">

<p class="ag-section-number">09 / PATTERN COMPOSITION</p>

## Composition Notes

PoI Guide normally occupies the first phase of a museum HMD-AR interaction sequence. It supports movement toward the point of interest and prepares the transition into indication, activation, and presentation.

A typical composition is:

<div class="ag-composition">
  <span>PoI Guide</span>
  <b>→</b>
  <span>Experience Indicator</span>
  <b>→</b>
  <span>Experience Presenter</span>
</div>

For example:

<div class="ag-composition">
  <span>Avatar Guide</span>
  <b>→</b>
  <span>Step-In Trigger</span>
  <b>→</b>
  <span>Sequential Explanation</span>
  <b>→</b>
  <span>AR Labelling</span>
</div>

or:

<div class="ag-composition">
  <span>Forward Cue-Routing</span>
  <b>→</b>
  <span>Exhibit Knowledge Trigger</span>
  <b>→</b>
  <span>AR Object Catching</span>
</div>

The handoff from guidance to activation should be explicit. When visitors arrive at the point of interest, the guidance cue should reduce intensity, stop, or transform into an arrival confirmation. The activation pattern should then become visually primary. This prevents visitors from confusing route following with exhibit interaction.

In multi-exhibit routes, the PoI Guide category can be repeated between points of interest, but each segment should have a clear start, route state, arrival state, and recovery behaviour.

</div>

<div class="ag-section" markdown="1">

<p class="ag-section-number">10 / TECHNICAL ALIGNMENT</p>

## Implementation Alignment

As a category-level pattern, PoI Guide should be implemented as a shared route-orchestration layer rather than as a single visual prefab. This layer can coordinate destination selection, waypoint data, route preview, guidance-state transitions, cue visibility, visitor-distance monitoring, turn anticipation, arrival detection, recovery behaviour, and handoff events.

Application-level prefabs such as **Avatar Guide** and **Forward Cue-Routing** can then subscribe to the same route state and event structure while rendering different guidance representations.

### Relevant Implementation Data

Relevant implementation data include:

- point-of-interest metadata;
- route geometry;
- waypoint lists;
- safe viewing positions;
- arrival zones;
- localization-confidence values;
- cue-state definitions;
- route-state definitions;
- feedback-channel settings;
- logging hooks.

### Implementation-Level Events

Implementation-level events may include:

<div class="ag-events">
  <span>Destination Selected</span>
  <span>Route Preview Shown</span>
  <span>Route Committed</span>
  <span>Guidance Started</span>
  <span>Cue Displayed</span>
  <span>Turn Anticipated</span>
  <span>Waypoint Reached</span>
  <span>Visitor Left Route</span>
  <span>Guidance Paused</span>
  <span>Recovery Started</span>
  <span>Tracking Confidence Low</span>
  <span>Arrival Confirmed</span>
  <span>Handoff Triggered</span>
  <span>Route Completed</span>
  <span>Guidance Ended</span>
</div>

These events can support debugging, system logs, observation sheets, and later evaluation of route completion, deviation frequency, missed cues, recovery success, arrival recognition, and transition success.

</div>

<div class="ag-section" markdown="1">

<p class="ag-section-number">11 / APPLICATION EXAMPLE</p>

## Example Use

In a natural-history museum, a visitor begins an HMD-AR experience and selects a whale skeleton as the next point of interest. The PoI Guide layer defines the route, previews the destination, and starts the guidance phase. Depending on the exhibition concept, this guidance may be instantiated as an **Avatar Guide** that visitors follow through the hall, or as **Forward Cue-Routing** that uses subtle floor-based ripples and directional sound cues.

As the visitor approaches the target area, the guidance state changes from navigation to arrival. The guide stops or the final route cue converges into an arrival marker. The guidance layer then hands over to an **Experience Indicator**, such as **Step-In Trigger** or **Exhibit Knowledge Trigger**, which activates the exhibit-related AR experience. After activation, the system continues into an **Experience Presenter** pattern, such as **Sequential Explanation** or **AR Labelling**.

</div>

</div>
