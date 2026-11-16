---
layout: pattern
title: "Experience Indicator"
category: "high-level"
pattern_category: indicator
pattern_group: experience-indicator
overlay: /images/PatternIcon/Initial Node.png
order: 2
tags:
  - Experience Indicator
  - AR Activation
  - Exhibit Discovery
thumbnail: /images/high_indicator.png
summary: "Making AR-enabled exhibits discoverable and activatable"
description: "The Experience Indicator category organizes HMD-AR activation patterns that help visitors recognize AR-enabled exhibits, understand available actions, confirm activation, and transition into exhibit-related AR experiences."
---

<div class="ag-pattern" markdown="1">

<div class="ag-hero" markdown="1">

<p class="ag-eyebrow">CATEGORY-LEVEL PATTERN · EXPERIENCE INDICATOR</p>

# Experience Indicator

<p class="ag-lead">
A category-level pattern class for making AR-enabled exhibits discoverable
and supporting the transition from arrival to activation.
</p>

<div class="ag-tags">
  <span>Experience Indicator</span>
  <span>AR Activation</span>
  <span>Exhibit Discovery</span>
  <span>Category-Level</span>
</div>

<div class="ag-hero-image">
  <img
    src="{{ '/images/HomePage/Fig_ExperienceIndicator.png' | relative_url }}"
    alt="Experience Indicator category illustration">
</div>

</div>

<div class="ag-section" markdown="1">

<p class="ag-section-number">01 / PATTERN DEFINITION</p>

## Pattern Identity

<div class="ag-metadata">
  <div>
    <span class="ag-meta-label">Name</span>
    <strong>Experience Indicator</strong>
  </div>
  <div>
    <span class="ag-meta-label">Level</span>
    <strong>Category-Level Pattern</strong>
  </div>
  <div>
    <span class="ag-meta-label">Category</span>
    <strong>Experience Indicator</strong>
  </div>
</div>

Category-level pattern class in the consolidated pattern system.

It groups application-level patterns that make AR-enabled exhibits discoverable and support the transition from noticing an opportunity to activating an HMD-AR experience.

### Intent

Help visitors discover, recognize, and activate AR experiences at points of interest through clear, consistent, and context-sensitive indicators.

The category supports the visitor journey from exhibit arrival to AR experience activation and can be instantiated through application-level patterns such as **Step-In Trigger** and **Exhibit Knowledge Trigger**.

</div>

<div class="ag-section" markdown="1">

<p class="ag-section-number">02 / DESIGN CHALLENGE</p>

## Problem and Rationale

<div class="ag-highlight-block" markdown="1">

### Problem

Visitors may overlook AR-enabled exhibits, hesitate after arriving at a point of interest, or fail to understand how an AR experience should be started. Physical exhibits do not always provide visible signs of interactivity, and HMD-based AR content may remain hidden until triggered.

If the activation opportunity is not clearly indicated, visitors may miss important content, waste time searching for controls, or require external assistance. If indicators are inconsistent or visually intrusive, they may disrupt the exhibition experience and reduce trust in the system.

A reusable indicator structure is therefore needed so that different activation mechanisms can support discoverability, confirmation, feedback, recovery, and handoff in a consistent way.

</div>

### Rationale

In HMD-based AR museums, visitors do not automatically know which exhibits contain AR content, where an AR experience begins, or what action is required to start it. This problem is especially important when only selected exhibits are augmented and when visitors are first-time HMD users.

The Experience Indicator class separates the general activation-support function from its concrete representation. This allows the system to maintain consistent discoverability, activation feedback, and lifecycle semantics across exhibits while allowing different activation forms, such as spatial entry zones, proximity triggers, concept-specific micro-tasks, voice prompts, or assisted activation.

As a category-level class, Experience Indicator defines the shared interaction role, variation dimensions, state logic, and composition position of activation patterns without requiring one fixed shape, distance, timing, or gesture.

</div>

<div class="ag-section" markdown="1">

<p class="ag-section-number">03 / APPLICABILITY</p>

## Context

This category applies to HMD-based AR museum and exhibition experiences in which visitors arrive at a point of interest and need to discover or activate exhibit-related AR content. It is especially relevant when:

- AR content is embedded in only some exhibits;
- the physical environment does not include explicit markers for AR interactivity;
- visitors explore freely or arrive through a guided route;
- different exhibits require different activation mechanisms;
- the system needs a consistent activation vocabulary across multiple exhibits;
- activation should hand over clearly to exhibit-related presentation or interaction patterns.

The category assumes that the system can identify relevant points of interest, display local indicators, and detect visitor activation through proximity, dwell, gesture, voice, selection, or a short task.

### Use When

Use this category-level pattern whenever an HMD-AR exhibit experience needs a clear transition from physical exhibit viewing to digital augmentation. It is appropriate when visitors must know that an AR experience is available, where they should stand or look, and what action will start the experience.

It is also useful when multiple exhibits in the same space require a consistent activation vocabulary while still allowing different activation mechanisms for different exhibit types.

<div class="ag-caution" markdown="1">

**Avoid When**

Do not rely on this category as a separate design layer when the AR content is always visible, when activation is automatic and requires no visitor interpretation, or when the exhibit context makes additional indicators unnecessary. In such cases, the activation function may be integrated directly into a presentation pattern.

</div>

</div>

<div class="ag-section" markdown="1">

<p class="ag-section-number">04 / DESIGN TRADE-OFFS</p>

## Forces

<div class="ag-forces" markdown="1">

### Discoverability vs. distraction

Indicators must stand out enough to be noticed, but should not clutter the scene or dominate the exhibit.

### Consistency vs. local adaptation

The system should use a recognizable visual and interaction language, while still adapting to different exhibits, layouts, and activation needs.

### Immediate feedback vs. subtlety

Activation should be confirmed clearly, but feedback should remain appropriate for the museum atmosphere.

### Automatic activation vs. visitor control

Proximity-based activation is easy to use, but explicit confirmation may be needed when accidental activation is likely.

### Accessibility vs. interaction richness

Activation cues should work for diverse visitors and device conditions, while still supporting richer concept-specific interactions when appropriate.

### Indicator persistence vs. visual cleanliness

Always-visible indicators increase discoverability, but on-demand or proximity-based indicators reduce visual clutter.

### Technical reliability vs. interpretive expressiveness

Simple triggers are robust, while richer knowledge-based triggers may communicate meaning more effectively but require more reliable interaction detection.

</div>

</div>

<div class="ag-section" markdown="1">

<p class="ag-section-number">05 / DESIGN RESPONSE</p>

## Solution

<div class="ag-solution" markdown="1">

Define a shared indicator logic that governs how visitors discover, approach, confirm, activate, and exit AR experiences at exhibits. The category should not prescribe one fixed shape, distance, timing, or gesture. Instead, it establishes system-level guarantees: AR opportunities should be discoverable without excessive clutter, activation states should be understandable, feedback should be immediate and multimodal where possible, and similar activation semantics should be reused across exhibits.

### Shared Activation Lifecycle

A typical lifecycle includes:

<div class="ag-composition">
  <span>Discover</span>
  <b>→</b>
  <span>Candidate</span>
  <b>→</b>
  <span>Confirm</span>
  <b>→</b>
  <span>Activate</span>
  <b>→</b>
  <span>Exit / Recover</span>
</div>

In the **Discover** state, the system signals that an exhibit has AR content. In the **Candidate** state, the visitor is close enough or oriented enough for the system to make the activation option more explicit. In the **Confirm** state, the visitor performs or completes the required activation condition. In the **Activate** state, the AR experience starts and the indicator hands over to the presentation layer. In the **Exit / Recover** state, the system allows visitors to leave, retry, or recover from failed activation.

Concrete application-level patterns instantiate this lifecycle differently. **Step-In Trigger** uses a spatial entry zone and dwell-based activation. **Exhibit Knowledge Trigger** uses a short concept-specific interaction to unlock deeper content. Other future indicators may use voice, gaze, object recognition, physical markers, or curator-assisted activation, as long as they preserve the shared discoverability, feedback, and handoff logic.

</div>

</div>

<div class="ag-section" markdown="1">

<p class="ag-section-number">06 / CONFIGURATION</p>

## Design Parameters and Recommended Settings

<div class="ag-param-highlights">

  <div class="ag-param-card">
    <strong>Placement</strong>
    <span>Indicator Visibility</span>
    <small>Ambient, anchored or on approach</small>
  </div>

  <div class="ag-param-card">
    <strong>Activation</strong>
    <span>Interaction Mode</span>
    <small>Proximity, dwell, gesture or task</small>
  </div>

  <div class="ag-param-card">
    <strong>Recovery</strong>
    <span>Activation Continuity</span>
    <small>Cancellation, tracking and retry</small>
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
        <td>Placement strategy</td>
        <td>Decide whether the indicator is ambient and visible from a distance, locally anchored near the exhibit, revealed only on approach, or tied to a specific interaction zone.</td>
      </tr>
      <tr>
        <td>Activation mode</td>
        <td>Use proximity, dwell, hand selection, gaze dwell, voice command, object manipulation, or concept-specific task completion depending on the intended level of agency and robustness.</td>
      </tr>
      <tr>
        <td>State visibility</td>
        <td>Define how the indicator changes between <strong>discoverable</strong>, <strong>candidate</strong>, <strong>confirmable</strong>, <strong>activated</strong>, <strong>inactive</strong>, and <strong>recovery</strong> states.</td>
      </tr>
      <tr>
        <td>Persistence level</td>
        <td>Decide whether indicators are always visible, shown on approach, revealed after guidance arrival, or hidden until the visitor looks toward the exhibit.</td>
      </tr>
      <tr>
        <td>Feedback mix</td>
        <td>Combine visual feedback with optional spatial audio, text prompts, animation, or body-based feedback where available. Use at least two feedback channels when accessibility or environmental uncertainty is important.</td>
      </tr>
      <tr>
        <td>Feedback intensity</td>
        <td>Tune glow, pulse, sound, motion, and label visibility so that activation is clear without producing abrupt transitions.</td>
      </tr>
      <tr>
        <td>False-activation prevention</td>
        <td>Use dwell time, confirmation steps, proximity thresholds, or task completion when accidental activation is likely.</td>
      </tr>
      <tr>
        <td>Accessibility settings</td>
        <td>Support readable labels, sufficient contrast, non-colour-dependent cues, adjustable audio, and alternative activation methods where possible.</td>
      </tr>
      <tr>
        <td>Recovery behaviour</td>
        <td>Define what happens when the visitor fails to activate, leaves the zone, loses tracking, or activates the wrong exhibit.</td>
      </tr>
      <tr>
        <td>Logging points</td>
        <td>Record discovery, approach, confirmation, activation, cancellation, recovery, and exit events to support usability analysis and system debugging.</td>
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

When applied successfully, the Experience Indicator category increases the discoverability of AR content, reduces hesitation at exhibits, and supports a smoother transition from physical viewing to digital interaction. It also provides a reusable activation vocabulary across an exhibition, making the AR system easier to learn for first-time visitors.

### Risks and Limitations

However, the category also introduces risks. Overuse of indicators can visually overload the exhibition space. Inconsistent activation semantics can confuse visitors and break expectations. Too much automation can reduce visitor control, while overly explicit confirmation can slow down the visit. The category therefore requires careful balancing of discoverability, subtlety, activation reliability, feedback clarity, and local exhibit meaning.

</div>

</div>

<div class="ag-section" markdown="1">

<p class="ag-section-number">08 / PATTERN LANGUAGE</p>

## Related Patterns

<div class="ag-related" markdown="1">

### Application-Level Patterns in This Category

**Step-In Trigger** instantiates this category through a floor-based entry zone that visitors enter to activate the AR experience.

**Exhibit Knowledge Trigger** instantiates this category through a short concept-specific interaction that unlocks deeper AR content.

### Preceding Guidance Patterns

**Avatar Guide** commonly precedes Experience Indicator by guiding visitors to the point of interest where an indicator becomes relevant.

**Forward Cue-Routing** commonly precedes Experience Indicator by guiding visitors through lightweight route cues before the indicator becomes active.

### Follow-up Presentation Patterns

**Sequential Explanation** commonly follows Experience Indicator after activation when visitors need structured exhibit-related content.

**AR Labelling** commonly follows Experience Indicator after activation when visitors need spatially anchored labels or component-level explanations.

**AR Exhibit Reassembler** commonly follows Experience Indicator when visitors should reconstruct missing or fragmented exhibit components.

**AR Exhibit Feature Drawing** commonly follows Experience Indicator when visitors should draw, trace, or mark interpretive exhibit features.

**AR Object Catching** commonly follows Experience Indicator when visitors should respond to virtual threats or objects around an exhibit.

</div>

</div>

<div class="ag-section" markdown="1">

<p class="ag-section-number">09 / PATTERN COMPOSITION</p>

## Composition Notes

Experience Indicator normally occupies the transition between guidance and presentation. A typical composition is:

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

The handoff from guidance should be clear. When visitors arrive at the point of interest, guidance cues should reduce intensity or end, and the indicator should become visually primary.

The handoff to presentation should also be explicit. Once activation succeeds, the indicator should fade, transform, or become secondary so that visitors understand that the main AR experience has begun. If several AR-enabled exhibits are nearby, only the relevant or nearest indicator should become active, while others remain hidden or shown less prominently.

</div>

<div class="ag-section" markdown="1">

<p class="ag-section-number">10 / TECHNICAL ALIGNMENT</p>

## Implementation Alignment

As a category-level pattern, Experience Indicator can be implemented as a shared activation-orchestration layer that coordinates exhibit availability, indicator visibility, activation state, confirmation logic, feedback, recovery, and handoff events.

Application-level prefabs such as **Step-In Trigger** and **Exhibit Knowledge Trigger** can subscribe to this shared state logic while using different visual representations and activation methods.

### Relevant Implementation Data

Relevant implementation data include:

- point-of-interest metadata;
- exhibit availability state;
- indicator anchors;
- activation zones;
- dwell thresholds;
- interaction-task definitions;
- feedback assets;
- fallback options;
- logging points.

### Implementation-Level Events

Implementation-level events may include:

<div class="ag-events">
  <span>Indicator Discovered</span>
  <span>Candidate Detected</span>
  <span>Visitor Approached</span>
  <span>Confirmation Started</span>
  <span>Confirmation Cancelled</span>
  <span>Activation Confirmed</span>
  <span>Experience Activated</span>
  <span>Activation Failed</span>
  <span>Recovery Shown</span>
  <span>Indicator Hidden</span>
  <span>Experience Exited</span>
</div>

These events can support debugging, usability observation, analytics, and comparison between different activation strategies.

</div>

<div class="ag-section" markdown="1">

<p class="ag-section-number">11 / APPLICATION EXAMPLE</p>

## Example Use

In a natural-history museum, visitors arrive near an AR-enabled whale exhibit after following a guidance pattern. The Experience Indicator class determines how the system reveals the activation opportunity.

In one version, the category is instantiated as a **Step-In Trigger**: a glowing floor circle appears at a safe viewing position, and the visitor activates the experience by stepping into it. In another version, it is instantiated as an **Exhibit Knowledge Trigger**: the visitor completes a short exhibit-related interaction before deeper content is unlocked.

In both versions, the indicator confirms activation and hands over to an **Experience Presenter** pattern such as **Sequential Explanation** or **AR Labelling**.

</div>

</div>
