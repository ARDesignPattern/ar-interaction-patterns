---
layout: pattern
title: "Avatar Guide"
category: "sub-level"
pattern_category: guiding
pattern_group: poi-guide
order: 1.1
tags:
  - PoI Guide
  - Experience Navigation
thumbnail: /images/Gif/FollowAvatar.gif
summary: "Guiding visitors to points of interest through a virtual companion"
description: "A virtual guide leads visitors toward a target point of interest, supports orientation and pacing, and hands over to activation or presentation patterns after arrival."
---

<div class="ag-pattern" markdown="1">

<div class="ag-hero" markdown="1">

<p class="ag-eyebrow">APPLICATION-LEVEL PATTERN · POINT OF INTEREST GUIDE</p>

# Avatar Guide

<p class="ag-lead">
A virtual companion that leads visitors toward a point of interest,
regulates walking pace, and supports the transition from movement
to exhibit engagement.
</p>

<div class="ag-tags">
  <span>PoI Guide</span>
  <span>Experience Navigation</span>
  <span>HMD-AR</span>
</div>

<div class="ag-hero-image">
  <img src="{{ '/images/Gif/FollowAvatar.gif' | relative_url }}"
       alt="Avatar Guide interaction demonstration">
</div>

</div>

<div class="ag-section" markdown="1">

<p class="ag-section-number">01 / PATTERN DEFINITION</p>

## Pattern Identity

<div class="ag-metadata">
  <div>
    <span class="ag-meta-label">Name</span>
    <strong>Avatar Guide</strong>
  </div>
  <div>
    <span class="ag-meta-label">Level</span>
    <strong>Application-Level Pattern</strong>
  </div>
  <div>
    <span class="ag-meta-label">Category</span>
    <strong>PoI Guide</strong>
  </div>
</div>

### Intent

Provide an embodied virtual guide that visitors can follow through the physical exhibition space. The pattern supports orientation, route following, pace regulation, and arrival recognition when visitors move toward a point of interest in an HMD-based AR museum experience.

</div>

<div class="ag-section" markdown="1">

<p class="ag-section-number">02 / DESIGN CHALLENGE</p>

## Problem and Rationale

<div class="ag-highlight-block" markdown="1">

### Problem

Visitors may lose orientation when moving between points of interest in an HMD-based AR museum experience. They may miss relevant exhibits, misunderstand the intended route, or fail to recognize when they have reached the correct destination. This problem is intensified by limited field of view, divided attention, unfamiliar HMD interaction, and variation in walking speed.

Simple route indicators can support direction, but they may not sufficiently regulate pacing or provide a clear sense of being accompanied through the exhibition. A more embodied guidance strategy is needed when visitors should be able to follow a visible guide and understand the transition from movement to arrival.

</div>

### Rationale

In HMD-based AR museum visits, visitors often need to move through a physical exhibition space while maintaining awareness of exhibits, other visitors, and digital guidance cues. Map-based or symbolic guidance can require interpretation, while static indicators may not support walking pace or route-following behaviour.

An avatar guide externalizes guidance as a visible moving entity. Visitors can follow the guide rather than continuously interpret arrows, maps, or interface panels. This makes guidance easier to perceive as a spatial relation between visitor, guide, route, and destination. The pattern is especially useful when the guide can also support a thematic or narrative framing of the museum experience.

</div>

<div class="ag-section" markdown="1">

<p class="ag-section-number">03 / APPLICABILITY</p>

## Context

This pattern applies to standing and walking HMD-based AR museum experiences in which visitors move from one location to another. It is especially relevant when:

- multiple points of interest are distributed across an exhibition area;
- visitors need guidance through a route, gallery, hall, or multi-point experience;
- the system can localize the visitor and position virtual content in relation to stable spatial anchors;
- a virtual character, companion, or thematic guide fits the exhibition concept;
- the guidance phase needs to connect clearly to later activation or content presentation.

The pattern assumes that the physical route is safe for visitors to follow while wearing an HMD and that the avatar can remain visible without blocking important exhibits or pathways.

### Use When

Use this pattern when:

- visitors need to be guided toward one or more points of interest;
- a visible guide is more appropriate than abstract path cues or directional markers;
- visitors may benefit from pace-regulated movement support;
- the museum experience benefits from a companion-like or narrative guide;
- the arrival point should trigger a clear transition into another interaction pattern, such as activation or exhibit-related presentation.

<div class="ag-caution" markdown="1">

**Avoid When**

Avoid using this pattern when the route is extremely short, when an avatar would visually distract from the exhibit, or when the exhibition space is too crowded or narrow for character-based guidance to remain comfortable and easy to follow.

</div>

</div>

<div class="ag-section" markdown="1">

<p class="ag-section-number">04 / DESIGN TRADE-OFFS</p>

## Forces

<div class="ag-forces" markdown="1">

### Guidance clarity vs. exhibit attention

The avatar must be visible enough to guide visitors, but not so visually dominant that it draws attention away from physical exhibits.

### Pacing vs. visitor autonomy

The avatar should support a comfortable walking pace without making visitors feel rushed or overly controlled.

### Social presence vs. distraction

A companion-like guide can strengthen engagement, but an overly expressive avatar may distract from the museum content.

### Animation quality vs. implementation cost

More believable avatar movement can improve acceptance, but complex animation may increase development effort and performance load.

### Spatial stability vs. real-world variability

The guide depends on reliable localization, route definition, and spatial anchoring, which may be affected by lighting, crowding, relocalization, or environmental change.

### Route structure vs. flexible exploration

The pattern can support a clear visitor journey, but should still allow visitors to pause, look around, or stop the guidance when needed.

</div>

</div>

<div class="ag-section" markdown="1">

<p class="ag-section-number">05 / DESIGN RESPONSE</p>

## Solution

<div class="ag-solution" markdown="1">

Implement a virtual guide that appears near the visitor or at the beginning of the route and moves along an authored path toward a target point of interest. The avatar should remain ahead of the visitor at a comfortable distance and adjust its behaviour according to the visitor’s position and movement.

The avatar should use clear movement states. During **active guidance** state, it moves along the path at a moderate speed and remains visible ahead of the visitor. In a **waiting** state, it pauses when the visitor slows down, looks away, or falls too far behind. In a **recovery** state, it provides a simple cue when the visitor deviates from the route or when tracking confidence becomes low. At the point of interest, it enters an **arrival** state, stops at a safe position, and provides clear visual or auditory feedback that the destination has been reached.

The avatar should not be overloaded with all presentation functions. Its primary role is to guide, pace, and announce arrival. After arrival, the experience may hand over to an activation pattern, such as **Step-In Trigger** or **Exhibit Knowledge Trigger**, and then to one or more presentation patterns, such as **Sequential Explanation** or **AR Labelling**. If the avatar remains visible during exhibit exploration, it should move into a quiet idle state or a clearly secondary support role.

</div>

</div>

<div class="ag-section" markdown="1">

<p class="ag-section-number">06 / CONFIGURATION</p>

## Design Parameters and Recommended Settings

<div class="ag-param-highlights">

  <div class="ag-param-card">
    <strong>2–3 m</strong>
    <span>Following Distance</span>
    <small>Practical default: 2.5 m</small>
  </div>

  <div class="ag-param-card">
    <strong>0.8–1.2 m/s</strong>
    <span>Walking Speed</span>
    <small>Adaptive, around 1.0 m/s</small>
  </div>

  <div class="ag-param-card">
    <strong>1.5–2.0 m</strong>
    <span>Arrival Radius</span>
    <small>Adjust to exhibit and activation position</small>
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
        <td>Following distance</td>
        <td>Maintain an approximate lead distance of <strong>2–3 metres</strong>, with <strong>2.5 metres</strong> as a practical default.</td>
      </tr>
      <tr>
        <td>Walking speed</td>
        <td>Use an adaptive walking speed around <strong>1.0 m/s</strong>, with a typical range of approximately <strong>0.8–1.2 m/s</strong>.</td>
      </tr>
      <tr>
        <td>Waypoint structure</td>
        <td>Define route waypoints in relation to stable spatial anchors, exhibit positions, and safe walking paths.</td>
      </tr>
      <tr>
        <td>Arrival radius</td>
        <td>Use an arrival radius of approximately <strong>1.5–2.0 metres</strong>, adjusted according to exhibit size, safe viewing distance, and the expected activation position for the next pattern.</td>
      </tr>
      <tr>
        <td>Avatar visibility</td>
        <td>Keep the avatar large and visually distinct enough to be recognized in the HMD field of view, but avoid excessive size, brightness, or animation intensity.</td>
      </tr>
      <tr>
        <td>Prompt timing</td>
        <td>Use gentle prompts only when needed, for example when the visitor hesitates, moves away from the intended route, or reaches a decision point.</td>
      </tr>
      <tr>
        <td>Feedback modalities</td>
        <td>Combine visual feedback with optional spatial audio or short verbal prompts.</td>
      </tr>
      <tr>
        <td>Control access</td>
        <td>Provide minimal visitor controls, such as <strong>Start</strong>, <strong>Pause</strong>, <strong>Resume</strong>, and <strong>End</strong>.</td>
      </tr>
      <tr>
        <td>State indication</td>
        <td>Use subtle animation, posture, position, or optional visual markers to distinguish between <strong>active guidance</strong>, <strong>waiting</strong>, <strong>paused</strong>, <strong>arrival</strong>, and <strong>recovery</strong> states.</td>
      </tr>
      <tr>
        <td>Fallback behaviour</td>
        <td>If localization, path following, or gesture input becomes unreliable, the avatar should stop in a safe state, provide a simple recovery cue, and allow the visitor to continue, restart, or end the guidance sequence.</td>
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

When applied successfully, the Avatar Guide can make spatial guidance more understandable, reduce the cognitive effort of interpreting route cues, and support a smoother transition from movement to exhibit engagement. It can also strengthen social presence and narrative coherence when the avatar’s visual identity is aligned with the museum theme or exhibition story.

### Risks and Limitations

However, the pattern also introduces risks. A highly visible avatar may distract from physical exhibits or reduce visitor autonomy if it appears too directive. Poor animation, unstable spatial registration, or delayed path updates may reduce trust in the system. In crowded or narrow spaces, the avatar may become visually distracting or difficult to follow. The pattern therefore requires careful tuning of visibility, distance, speed, feedback, and fallback behaviour.

</div>

</div>

<div class="ag-section" markdown="1">

<p class="ag-section-number">08 / PATTERN LANGUAGE</p>

## Related Patterns

<div class="ag-related" markdown="1">

### Alternative Guidance Pattern

**Forward Cue-Routing** provides a more lightweight guidance strategy under the same PoI Guide category. It can be used when the experience requires route guidance but should avoid a socially or narratively prominent avatar.

### Follow-up Activation Patterns

**Step-In Trigger** can follow the Avatar Guide after arrival when the visitor should enter the next AR experience through a spatial trigger zone.

**Exhibit Knowledge Trigger** can follow the Avatar Guide when activation should be tied more directly to exhibit-related information or knowledge cues.

### Follow-up Presentation Patterns

**Sequential Explanation** can follow the guidance phase when visitors reach the target exhibit and need structured step-by-step content.

**AR Labelling** can follow the guidance phase when visitors need spatially placed labels or annotations connected to parts of the physical exhibit.

</div>

</div>

<div class="ag-section" markdown="1">

<p class="ag-section-number">09 / PATTERN COMPOSITION</p>

## Composition Notes

The Avatar Guide is usually placed at the beginning of a museum HMD-AR interaction sequence. A typical composition is:

<div class="ag-composition">
  <span>Avatar Guide</span>
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

The handoff after arrival should be explicit. The avatar may stop, turn toward the exhibit, provide a short arrival cue, and then allow a trigger zone, knowledge marker, or presentation interface to become active. This prevents visitors from confusing the guiding phase with the content exploration phase.

The Avatar Guide should remain focused on movement, pacing, and arrival. It should not take over the full content presentation role unless this is deliberately designed as a separate extension.

</div>

<div class="ag-section" markdown="1">

<p class="ag-section-number">10 / TECHNICAL ALIGNMENT</p>

## Implementation Alignment

The pattern can be implemented as a reusable guidance module or Unity prefab that combines:

- an avatar object;
- waypoint-based path logic;
- movement-state control;
- visitor-distance monitoring;
- arrival detection;
- event-based handoff to subsequent modules.

Relevant exposed parameters include following distance, movement speed, waypoint list, arrival radius, avatar scale, visibility settings, prompt timing, audio use, and fallback thresholds.

### Implementation-Level Events

Implementation-level events may include:

<div class="ag-events">
  <span>Guidance Started</span>
  <span>Waypoint Reached</span>
  <span>Visitor Too Far</span>
  <span>Visitor Returned</span>
  <span>Guidance Paused</span>
  <span>Guidance Resumed</span>
  <span>Arrival Reached</span>
  <span>Tracking Lost</span>
  <span>Guidance Ended</span>
</div>

These events can support debugging, system logs, observation sheets, and later evaluation.

{% assign avatar_implementation = site.technology | where: "title", "Avatar Guide" | first %}

{% if avatar_implementation %}

<div class="ag-implementation-link">
  <div>
    <strong>Unity Implementation Available</strong>
    <p>Guide Avatar · UnityPackage v1.0.1</p>
  </div>
  <a href="{{ avatar_implementation.url | relative_url }}">
    View Implementation →
  </a>
</div>
{% endif %}

</div>

<div class="ag-section" markdown="1">

<p class="ag-section-number">11 / APPLICATION EXAMPLE</p>

## Example Use

In a natural-history museum, a small virtual guide appears near the visitor at the beginning of an HMD-AR experience and leads them toward a large whale skeleton. The guide moves along a predefined route, pauses when the visitor stops to look around, and waits at decision points until the visitor approaches again. Upon arrival, the guide stops at a safe viewing distance, turns toward the exhibit, and confirms that the visitor has reached the whale. A spatial activation cue then appears near the exhibit, allowing the visitor to enter the next part of the AR experience through a **Step-In Trigger**. After activation, exhibit-related information is presented through **Sequential Explanation** and **AR Labelling**.

<div class="ag-video">
  <iframe
    src="https://www.youtube-nocookie.com/embed/UfcltoRAjKA"
    title="Avatar Guide - Example Use"
    loading="lazy"
    frameborder="0"
    allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture"
    allowfullscreen>
  </iframe>
</div>

</div>

</div>
