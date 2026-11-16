---
layout: pattern
title: "Step-In Trigger"
category: "sub-level"
pattern_category: indicator
pattern_group: experience-indicator
order: 2.1
tags:
  - Experience Indicator
  - Spatial Trigger
thumbnail: /images/Gif/EnteringCircle.gif
summary: "Activating AR content through a floor-based spatial entry zone"
description: "A floor-based entry zone makes AR-enabled exhibits discoverable and allows visitors to activate an HMD-AR experience through natural embodied movement."
---

<div class="ag-pattern" markdown="1">

<div class="ag-hero" markdown="1">

<p class="ag-eyebrow">APPLICATION-LEVEL PATTERN · EXPERIENCE INDICATOR</p>

# Step-In Trigger

<p class="ag-lead">
A floor-based entry zone that indicates and activates AR exhibit
experiences through embodied movement.
</p>

<div class="ag-tags">
  <span>Experience Indicator</span>
  <span>Spatial Trigger</span>
  <span>HMD-AR</span>
</div>

<div class="ag-hero-image">
  <img
    src="{{ '/images/Gif/EnteringCircle.gif' | relative_url }}"
    alt="Step-In Trigger interaction demonstration">
</div>

</div>

<div class="ag-section" markdown="1">

<p class="ag-section-number">01 / PATTERN DEFINITION</p>

## Pattern Identity

<div class="ag-metadata">
  <div>
    <span class="ag-meta-label">Name</span>
    <strong>Step-In Trigger</strong>
  </div>
  <div>
    <span class="ag-meta-label">Level</span>
    <strong>Application-Level Pattern</strong>
  </div>
  <div>
    <span class="ag-meta-label">Category</span>
    <strong>Experience Indicator</strong>
  </div>
</div>

### Intent

Provide a floor-based spatial entry zone that indicates where an HMD-AR exhibit experience can be activated and allows visitors to start the experience through natural embodied movement rather than through complex gestures, handheld controls, or menu-based interaction.

</div>

<div class="ag-section" markdown="1">

<p class="ag-section-number">02 / DESIGN CHALLENGE</p>

## Problem and Rationale

<div class="ag-highlight-block" markdown="1">

### Problem

Visitors may overlook AR-enabled exhibits, hesitate after arriving at a point of interest, or fail to understand how to activate the corresponding AR content. This problem is especially likely when only selected exhibits are augmented and when the digital content remains invisible until activation.

Gesture-based or menu-based activation can increase the learning burden for first-time HMD users. A more direct and embodied activation strategy is needed when visitors should be able to start the AR experience by moving naturally into a clearly marked spatial zone.

</div>

### Rationale

In HMD-based AR museum visits, visitors do not automatically know which exhibits contain AR content or how an AR experience should be started. A visible entry zone on the floor provides a simple spatial convention: visitors can understand that stepping into the zone means entering or launching the AR experience.

The pattern uses proximity and short dwell-based activation to reduce the need for explicit menu interaction. It supports low-effort activation for first-time users and creates a clear transition from noticing an AR opportunity to starting the exhibit-related experience.

</div>

<div class="ag-section" markdown="1">

<p class="ag-section-number">03 / APPLICABILITY</p>

## Context

This pattern applies to HMD-based AR museum experiences in which visitors arrive near a point of interest and need to recognize that an AR experience is available. It is especially relevant when:

- only selected exhibits provide AR content;
- visitors freely explore the exhibition without a fixed interaction sequence;
- the activation opportunity needs to be visible from a short distance;
- the museum wants to avoid handheld controls or complex gesture input;
- the AR experience should begin at a safe and meaningful viewing position.

The pattern assumes that the system can detect the visitor’s position reliably enough to determine whether they have entered and remained inside the trigger zone.

### Use When

Use this pattern when:

- visitors need a clear and easy-to-use way to activate an AR exhibit experience;
- the intended action can be communicated through a spatial entry zone;
- stepping into a floor-based circle or marker fits the exhibition layout;
- the activation should feel embodied and hands-free;
- the experience should transition smoothly from arrival to presentation.

<div class="ag-caution" markdown="1">

**Avoid When**

Avoid using this pattern when the floor is visually cluttered, crowded, unsafe, or unsuitable for spatial markers. It may also be less appropriate when activation should require a meaningful exhibit-related action rather than simple spatial entry; in that case, **Exhibit Knowledge Trigger** may be more suitable.

</div>

</div>

<div class="ag-section" markdown="1">

<p class="ag-section-number">04 / DESIGN TRADE-OFFS</p>

## Forces

<div class="ag-forces" markdown="1">

### Discoverability vs. visual subtlety

The trigger zone must be noticeable enough to invite action, but not so bright or large that it clutters the floor or distracts from the exhibit.

### Activation reliability vs. visitor freedom

The system must detect entry reliably, while avoiding accidental activation when visitors only pass nearby.

### Easy-to-use interaction vs. meaningful engagement

A simple step-in action is easy to understand, but may provide less interpretive meaning than a concept-linked activation task.

### Feedback clarity vs. interruption

Activation feedback should clearly confirm that the experience has started, but should not interrupt the museum flow with excessive effects.

### Spatial placement vs. safety

The trigger zone should be close enough to the exhibit to feel meaningful, but far enough to preserve safe viewing distance and visitor circulation.

### Automation vs. visitor control

Automatic activation can feel seamless, but visitors should still understand what has happened and how to exit or continue.

</div>

</div>

<div class="ag-section" markdown="1">

<p class="ag-section-number">05 / DESIGN RESPONSE</p>

## Solution

<div class="ag-solution" markdown="1">

Place a visible virtual circle or entry marker on the floor in front of the AR-enabled exhibit. The marker should indicate that the visitor can start the AR experience by stepping into the zone.

The trigger zone should be positioned at a safe and meaningful viewing distance from the exhibit. A label, icon, preview model, or short prompt may be placed near the marker to communicate what experience is available. The visual design should be noticeable but not visually dominant.

When the visitor enters the zone, the system begins a short dwell check to avoid false activation. If the visitor remains inside the zone for the required dwell duration, the activation is confirmed. The system then provides multimodal feedback, such as a pulse animation, short spatial audio cue, label change, or fade-out of the trigger marker.

After activation, the trigger elements should fade, transform, or become secondary so that visitors understand that the main AR experience has begun. The pattern should then hand over to a presentation pattern such as **Sequential Explanation**, **AR Labelling**, or another exhibit-related interaction pattern.

</div>

</div>

<div class="ag-section" markdown="1">

<p class="ag-section-number">06 / CONFIGURATION</p>

## Design Parameters and Recommended Settings

<div class="ag-param-highlights">

  <div class="ag-param-card">
    <strong>0.6–1.2 m</strong>
    <span>Circle Radius</span>
    <small>Practical default: 0.9 m</small>
  </div>

  <div class="ag-param-card">
    <strong>0.40 s</strong>
    <span>Dwell Time</span>
    <small>Stable dwell threshold</small>
  </div>

  <div class="ag-param-card">
    <strong>0.8–1.2 m</strong>
    <span>Placement from Exhibit</span>
    <small>From the exhibit's front edge</small>
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
        <td>Circle radius</td>
        <td>
          Use a radius of approximately
          <strong>0.6–1.2 metres</strong>, with
          <strong>0.9 metres</strong> as a practical default.
        </td>
      </tr>

      <tr>
        <td>Dwell time</td>
        <td>
          Use a short stable dwell threshold of approximately
          <strong>0.40 seconds</strong> after the visitor
          enters the zone.
        </td>
      </tr>

      <tr>
        <td>Placement from exhibit</td>
        <td>
          Place the circle centre approximately
          <strong>0.8–1.2 metres</strong> from the exhibit’s
          front edge, adjusted according to exhibit size,
          safe viewing distance, and visitor flow.
        </td>
      </tr>

      <tr>
        <td>Detection threshold</td>
        <td>
          Define the entry condition based on visitor position,
          feet or head projection, or another stable
          body-position reference.
        </td>
      </tr>

      <tr>
        <td>Label height</td>
        <td>
          Place title labels or short prompts at approximately
          <strong>0.5 metres</strong> above the floor or in
          another peripheral but readable position.
        </td>
      </tr>

      <tr>
        <td>Preview element</td>
        <td>
          Optionally include a small 3D model, icon, or animation
          that previews the available AR content.
        </td>
      </tr>

      <tr>
        <td>Visual style</td>
        <td>
          Use a clear but low-clutter visual form, such as a
          glowing ring, pulsing outline, soft disc, or
          thematic floor marker.
        </td>
      </tr>

      <tr>
        <td>Pulse speed</td>
        <td>
          Keep pulsing slow and subtle enough to attract
          attention without creating visual fatigue.
        </td>
      </tr>

      <tr>
        <td>Audio cue</td>
        <td>
          Use a short spatial audio cue, such as a chime,
          splash, or thematic sound, to confirm activation.
        </td>
      </tr>

      <tr>
        <td>Fade duration</td>
        <td>
          Use an optional fade-out of approximately
          <strong>0.5 seconds</strong> for the circle,
          label, and preview element after activation.
        </td>
      </tr>

      <tr>
        <td>Activation state</td>
        <td>
          Distinguish between at least
          <strong>available</strong>,
          <strong>entered</strong>,
          <strong>dwell started</strong>,
          <strong>activated</strong>, and
          <strong>completed</strong> states.
        </td>
      </tr>

      <tr>
        <td>Fallback behaviour</td>
        <td>
          If tracking becomes unstable or the visitor exits
          the zone before dwell completion, cancel activation
          without disrupting the experience and keep
          the marker available.
        </td>
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

When applied successfully, the Step-In Trigger makes AR-enabled exhibits easier to discover and start. It reduces reliance on gesture menus or handheld controls and supports a natural embodied action that first-time HMD users can understand quickly. The pattern also creates a clear transition from arrival at the exhibit to activation of the AR experience.

### Risks and Limitations

However, the pattern can also create problems if the trigger zone is too large, too bright, too dense, or too close to visitor pathways. Visitors may accidentally activate content when passing by, or may miss the marker if it is too subtle. If spatial tracking is unstable, the circle may appear misaligned or activation may fail. The pattern therefore requires careful tuning of radius, placement, dwell time, feedback, and fallback behaviour.

</div>

</div>

<div class="ag-section" markdown="1">

<p class="ag-section-number">08 / PATTERN LANGUAGE</p>

## Related Patterns

<div class="ag-related" markdown="1">

### Alternative Activation Pattern

**Exhibit Knowledge Trigger** is an alternative Experience Indicator pattern. It is more suitable when activation should involve a short exhibit-related action or concept-linked micro-task rather than simple spatial entry.

### Preceding Guidance Patterns

**Avatar Guide** can precede Step-In Trigger by guiding visitors to the point of interest where the trigger zone becomes active.

**Forward Cue-Routing** can precede Step-In Trigger by guiding visitors through lightweight route cues and handing over to the trigger zone at the destination.

### Follow-up Presentation Patterns

**Sequential Explanation** can follow Step-In Trigger when the activated experience should present structured content step by step.

**AR Labelling** can follow Step-In Trigger when visitors need spatially placed labels or annotations connected to parts of the physical exhibit.

**AR Exhibit Reassembler** can follow Step-In Trigger when the activated experience involves reconstructing or assembling exhibit-related elements.

**AR Exhibit Feature Drawing** can follow Step-In Trigger when the activated experience involves drawing, highlighting, or sketching exhibit features in AR.

**AR Object Catching** can follow Step-In Trigger when the activated experience involves catching, removing, or responding to virtual objects around the exhibit.

</div>

</div>

<div class="ag-section" markdown="1">

<p class="ag-section-number">09 / PATTERN COMPOSITION</p>

## Composition Notes

Step-In Trigger normally occupies the transition between arrival and exhibit-related AR presentation. A typical composition is:

<div class="ag-composition">
  <span>PoI Guide</span>
  <b>→</b>
  <span>Step-In Trigger</span>
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

The handoff from guidance should be explicit. When visitors arrive at the point of interest, guidance cues should reduce intensity or end, and the Step-In Trigger should become visually primary.

The handoff to presentation should also be clear. Once activation succeeds, the circle, label, and preview elements should fade out or become secondary so that visitors understand that the main AR experience has begun.

If several AR-enabled exhibits are nearby, only the relevant or nearest Step-In Trigger should be active, while other trigger zones remain hidden or made less visible.

</div>

<div class="ag-section" markdown="1">

<p class="ag-section-number">10 / TECHNICAL ALIGNMENT</p>

## Implementation Alignment

The pattern can be implemented as a reusable spatial-trigger module or Unity prefab that combines:

- a floor circle object;
- position detection;
- dwell-time logic;
- feedback animation;
- optional spatial audio;
- preview content;
- activation-state control;
- event-based handoff to subsequent modules.

Relevant exposed parameters include circle radius, circle position, placement offset from the exhibit, dwell time, detection threshold, visual style, transparency, pulse speed, label text, label height, preview element, audio cue, fade duration, activation state, and fallback behaviour.

### Implementation-Level Events

Implementation-level events may include:

<div class="ag-events">
  <span>Circle Shown</span>
  <span>Visitor Entered Circle</span>
  <span>Visitor Exited Circle</span>
  <span>Dwell Started</span>
  <span>Dwell Cancelled</span>
  <span>Activation Confirmed</span>
  <span>Feedback Played</span>
  <span>Circle Faded</span>
  <span>Tracking Unstable</span>
  <span>Experience Launched</span>
</div>

These events can support debugging, system logs, observation sheets, and later evaluation of discoverability, missed activation, false activation, dwell time, hesitation, and transition success.

{% assign stepin_implementation = site.technology | where: "title", "Step-In Trigger" | first %}

{% if stepin_implementation %}

<div class="ag-implementation-link">
  <div>
    <strong>Unity Implementation Available</strong>
    <p>Floor Circle Indicator · UnityPackage v1.0</p>
  </div>
  <a href="{{ stepin_implementation.url | relative_url }}">
    View Implementation →
  </a>
</div>
{% endif %}

</div>

<div class="ag-section" markdown="1">

<p class="ag-section-number">11 / APPLICATION EXAMPLE</p>

## Example Use

In a natural-history museum, a glowing circular marker appears on the floor in front of a whale or orca exhibit. A small label and a subtle preview model indicate that an AR experience is available. When the visitor steps into the circle and remains there briefly, the circle pulses, a short spatial audio cue confirms activation, and the indicator elements fade out.

The system then launches the exhibit-related AR experience, for example a **Sequential Explanation** that presents interpretive content or an **AR Labelling** sequence that highlights different anatomical features of the exhibit.

<div class="ag-video">
  <iframe
    src="https://www.youtube-nocookie.com/embed/CtplECOaHXc"
    title="Step-In Trigger - Example Use"
    loading="lazy"
    frameborder="0"
    allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture"
    allowfullscreen>
  </iframe>
</div>

</div>

</div>
