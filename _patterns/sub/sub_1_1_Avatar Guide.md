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

<div class="column">
  <img src="{{ '/images/Gif/FollowAvatar.gif' | relative_url }}" alt="Avatar Guide" class="profile">
</div> 

# Avatar Guide

A virtual companion that leads visitors toward a point of interest, regulates walking pace, and supports the transition from movement to exhibit engagement.

---

## Name

Avatar Guide

---

## Level and Category

Application-level pattern under the category-level class **PoI Guide**.

---

## Intent

Provide an embodied virtual guide that visitors can follow through the physical exhibition space. The pattern supports orientation, route following, pace regulation, and arrival recognition when visitors move toward a point of interest in an HMD-based AR museum experience.

---

## Rationale

In HMD-based AR museum visits, visitors often need to move through a physical exhibition space while maintaining awareness of exhibits, other visitors, and digital guidance cues. Map-based or symbolic guidance can require interpretation, while static indicators may not support walking pace or route-following behaviour.

An avatar guide externalizes guidance as a visible moving entity. Visitors can follow the guide rather than continuously decode arrows, maps, or interface panels. This makes guidance easier to perceive as a spatial relation between visitor, guide, route, and destination. The pattern is especially useful when the guide can also support a thematic or narrative framing of the museum experience.

---

## Problem

Visitors may lose orientation when moving between points of interest in an HMD-based AR museum experience. They may miss relevant exhibits, misunderstand the intended route, or fail to recognize when they have reached the correct destination. This problem is intensified by limited field of view, divided attention, unfamiliar HMD interaction, and variation in walking speed.

Simple route indicators can support direction, but they may not sufficiently regulate pacing or provide a clear sense of being accompanied through the exhibition. A more embodied guidance strategy is needed when visitors should be able to follow a visible guide and understand the transition from movement to arrival.

---

## Context

This pattern applies to standing and walking HMD-based AR museum experiences in which visitors move from one location to another. It is especially relevant when:

- multiple points of interest are distributed across an exhibition area;
- visitors need guidance through a route, gallery, hall, or multi-point experience;
- the system can localize the visitor and position virtual content in relation to stable spatial anchors;
- a virtual character, companion, or thematic guide fits the exhibition concept;
- the guidance phase needs to connect clearly to later activation or content presentation.

The pattern assumes that the physical route is safe for visitors to follow while wearing an HMD and that the avatar can remain visible without blocking important exhibits or pathways.

---

## Use When

Use this pattern when:

- visitors need to be guided toward one or more points of interest;
- a visible guide is more appropriate than abstract path cues or directional markers;
- visitors may benefit from pace-regulated movement support;
- the museum experience benefits from a companion-like or narrative guide;
- the arrival point should trigger a clear transition into another interaction pattern, such as activation or exhibit-related presentation.

Avoid using this pattern when the route is extremely short, when an avatar would visually distract from the exhibit, or when the exhibition space is too crowded or narrow for character-based guidance to remain comfortable and legible.

---

## Forces

- **Guidance clarity vs. exhibit attention:** The avatar must be visible enough to guide visitors, but not so visually dominant that it draws attention away from physical exhibits.
- **Pacing vs. visitor autonomy:** The avatar should support a comfortable walking pace without making visitors feel rushed or overly controlled.
- **Social presence vs. distraction:** A companion-like guide can strengthen engagement, but an overly expressive avatar may distract from the museum content.
- **Animation quality vs. implementation cost:** More believable avatar movement can improve acceptance, but complex animation may increase development effort and performance load.
- **Spatial stability vs. real-world variability:** The guide depends on reliable localization, route definition, and spatial anchoring, which may be affected by lighting, crowding, relocalization, or environmental change.
- **Route structure vs. flexible exploration:** The pattern can support a clear visitor journey, but should still allow visitors to pause, look around, or stop the guidance when needed.

---

## Solution

Implement a virtual guide that appears near the visitor or at the beginning of the route and moves along an authored path toward a target point of interest. The avatar should remain ahead of the visitor at a comfortable distance and adjust its behaviour according to the visitor’s position and movement.

The avatar should use clear movement states. In an **en-route** state, it moves along the path at a moderate speed and remains visible ahead of the visitor. In a **waiting** state, it pauses when the visitor slows down, looks away, or falls too far behind. In a **recovery** state, it provides a simple cue when the visitor deviates from the route or when tracking confidence becomes low. At the point of interest, it enters an **arrival** state, stops at a safe position, and provides clear visual or auditory feedback that the destination has been reached.

The avatar should not be overloaded with all presentation functions. Its primary role is to guide, pace, and announce arrival. After arrival, the experience may hand over to an activation pattern, such as **Step-In Trigger** or **Exhibit Knowledge Trigger**, and then to one or more presentation patterns, such as **Sequential Explanation** or **AR Labelling**. If the avatar remains visible during exhibit exploration, it should move into a quiet idle state or a clearly secondary support role.

---

## Design Parameters and Recommended Settings

- **Following distance:** Maintain an approximate lead distance of **2–3 metres**, with **2.5 metres** as a practical default.
- **Walking speed:** Use an adaptive walking speed around **1.0 m/s**, with a typical range of approximately **0.8–1.2 m/s**.
- **Waypoint structure:** Define route waypoints in relation to stable spatial anchors, exhibit positions, and safe walking paths.
- **Arrival radius:** Use an arrival radius of approximately **1.5–2.0 metres**, adjusted according to exhibit size, safe viewing distance, and the expected activation position for the next pattern.
- **Avatar visibility:** Keep the avatar large and visually distinct enough to be recognized in the HMD field of view, but avoid excessive size, brightness, or animation intensity.
- **Prompt cadence:** Use gentle prompts only when needed, for example when the visitor hesitates, deviates, or reaches a decision point.
- **Feedback modalities:** Combine visual feedback with optional spatial audio or short verbal prompts.
- **Control access:** Provide minimal visitor controls, such as **Start**, **Pause**, **Resume**, and **End**.
- **State indication:** Use subtle animation, posture, position, or optional visual markers to distinguish between **en-route**, **waiting**, **paused**, **arrival**, and **recovery** states.
- **Fallback behaviour:** If localization, path following, or gesture input becomes unreliable, the avatar should stop in a safe state, provide a simple recovery cue, and allow the visitor to continue, restart, or end the guidance sequence.

---

## Consequences

When applied successfully, the Avatar Guide can make spatial guidance more understandable, reduce the cognitive effort of interpreting route cues, and support a smoother transition from movement to exhibit engagement. It can also strengthen social presence and narrative coherence when the avatar’s visual identity is aligned with the museum theme or exhibition story.

However, the pattern also introduces risks. A highly visible avatar may distract from physical exhibits or reduce visitor autonomy if it appears too directive. Poor animation, unstable spatial registration, or delayed path updates may reduce trust in the system. In crowded or narrow spaces, the avatar may become visually intrusive or difficult to follow. The pattern therefore requires careful tuning of visibility, distance, speed, feedback, and fallback behaviour.

---

## Related Patterns

- **Alternative guidance pattern**
  - **Forward Cue-Routing** provides a more lightweight guidance strategy under the same PoI Guide category. It can be used when the experience requires route guidance but should avoid a socially or narratively prominent avatar.

- **Follow-up activation patterns**
  - **Step-In Trigger** can follow the Avatar Guide after arrival when the visitor should enter the next AR experience through a spatial trigger zone.
  - **Exhibit Knowledge Trigger** can follow the Avatar Guide when activation should be tied more directly to exhibit-related information or knowledge cues.

- **Follow-up presentation patterns**
  - **Sequential Explanation** can follow the guidance phase when visitors reach the target exhibit and need structured step-by-step content.
  - **AR Labelling** can follow the guidance phase when visitors need spatially placed labels or annotations connected to parts of the physical exhibit.

---

## Composition Notes

The Avatar Guide is usually placed at the beginning of a museum HMD-AR interaction sequence. A typical composition is:

**Avatar Guide → Experience Indicator → Experience Presenter**

For example:

**Avatar Guide → Step-In Trigger → Sequential Explanation → AR Labelling**

The handoff after arrival should be explicit. The avatar may stop, turn toward the exhibit, provide a short arrival cue, and then allow a trigger zone, knowledge marker, or presentation interface to become active. This prevents visitors from confusing the guiding phase with the content exploration phase.

The Avatar Guide should remain focused on movement, pacing, and arrival. It should not take over the full content presentation role unless this is deliberately designed as a separate extension.

---

## Implementation Alignment

The pattern can be implemented as a reusable guidance module or Unity prefab that combines:

- an avatar object;
- waypoint-based path logic;
- movement-state control;
- visitor-distance monitoring;
- arrival detection;
- event-based handoff to subsequent modules.

Relevant exposed parameters include following distance, movement speed, waypoint list, arrival radius, avatar scale, visibility settings, prompt timing, audio use, and fallback thresholds.

Implementation-level events may include:

- guidance started;
- waypoint reached;
- visitor too far;
- visitor returned;
- guidance paused;
- guidance resumed;
- arrival reached;
- tracking lost;
- guidance ended.

These events can support debugging, system logs, observation sheets, and later evaluation.

---

## Example Use

In a natural-history museum, a small virtual guide appears near the visitor at the beginning of an HMD-AR experience and leads them toward a large whale skeleton. The guide moves along a predefined route, pauses when the visitor stops to look around, and waits at decision points until the visitor approaches again. Upon arrival, the guide stops at a safe viewing distance, turns toward the exhibit, and confirms that the visitor has reached the whale. A spatial activation cue then appears near the exhibit, allowing the visitor to enter the next part of the AR experience through a **Step-In Trigger**. After activation, exhibit-related information is presented through **Sequential Explanation** and **AR Labelling**.

<div class="intro-video-wrapper">
  <iframe
    src="https://www.youtube-nocookie.com/embed/UfcltoRAjKA"
    title="YouTube video player"
    frameborder="0"
    allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture"
    allowfullscreen
  ></iframe>
</div>