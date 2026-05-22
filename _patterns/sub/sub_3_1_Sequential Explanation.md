---
layout: pattern
title: "Sequential Explanation"
category: "sub-level"
pattern_category: presenter
pattern_group: experience-presenter
order: 3.1

tags:
  - Experience Presenter
  - Sequential Content
thumbnail: /images/Gif/SequentialExploration.gif
summary: "Presenting exhibit information through structured, self-paced steps"
description: "A step-by-step AR interface organizes exhibit information into manageable content units and lets visitors move through explanation sequences at their own pace."
---

<div class="column">
  <img src="{{ '/images/Gif/SequentialExploration.gif' | relative_url }}" alt="Sequential Explanation" class="profile">
</div> 

# Sequential Explanation

A step-by-step AR presentation structure that lets visitors explore exhibit information in a clear order and at their own pace.

---

## Name

Sequential Explanation

---

## Level and Category

Application-level pattern under the category-level class **Experience Presenter**.

---

## Intent

Present exhibit information through a structured, step-by-step AR interface that allows visitors to explore multiple content segments in a clear order and at their own pace.

---

## Rationale

Museum exhibits often contain multiple layers of information, such as historical background, anatomical structure, ecological function, behavioural explanation, or curatorial interpretation. In HMD-based AR, presenting all of these layers at once can overload visitors, especially under limited field of view and short interaction time.

Sequential Explanation reduces this complexity by dividing content into ordered, bite-sized steps and by providing explicit navigation controls. This supports a predictable mental model of the information structure while preserving visitor control over pacing, repetition, and skipping.

---

## Problem

Visitors may struggle to understand exhibits when information is dense, multi-layered, or distributed across several visual and auditory elements. Without a clear sequence, visitors may miss key details, lose the relationship between content segments, or become uncertain about what to attend to next.

In HMD-based AR, this problem is intensified by limited field of view, divided attention between the physical exhibit and digital overlays, and unfamiliar interaction controls. A structured explanation flow is needed when exhibit content should be presented in a manageable and revisitable order.

---

## Context

This pattern applies to HMD-based AR museum experiences after visitors have reached and activated a point of interest. It is especially relevant when:

- the exhibit contains multiple information categories or content layers;
- the AR experience needs to present text, images, 3D models, animation, audio, or spatial highlights in a controlled order;
- visitors should be able to move through the explanation at their own pace;
- the content requires a beginning, middle, and end rather than free exploration alone;
- the system needs to support revisitation, skipping, or repetition of individual content units.

The pattern assumes that the exhibit-related AR experience has already been activated, for example through **Step-In Trigger** or **Exhibit Knowledge Trigger**.

---

## Use When

Use this pattern when:

- visitors need structured access to exhibit information after activation;
- the content is too dense to present all at once;
- the museum wants to guide visitors through a coherent interpretive sequence;
- visitors should be able to use clear **Previous** and **Next** controls;
- content segments should remain modular, repeatable, and easy to update;
- the experience should support self-paced learning rather than automatic time-based progression.

Avoid using this pattern when the experience depends mainly on free spatial exploration, open-ended manipulation, or playful task completion. In such cases, **AR Labelling**, **AR Exhibit Reassembler**, **AR Exhibit Feature Drawing**, or **AR Object Catching** may be more suitable as the primary presentation pattern.

---

## Forces

- **Structure vs. exploration:** A clear sequence supports understanding, but too much linearity may reduce visitor freedom.
- **Information depth vs. cognitive load:** Content should be rich enough to be meaningful, but not so dense that visitors feel overwhelmed.
- **Pacing control vs. narrative coherence:** Visitors should control the pace, while the sequence should still maintain a coherent interpretive flow.
- **UI clarity vs. exhibit attention:** Navigation controls must be easy to find without drawing excessive attention away from the physical exhibit.
- **Media richness vs. readability:** Text, images, 3D models, audio, and animation should complement each other rather than compete.
- **Consistency vs. local adaptation:** Navigation should remain consistent across steps, while content layout may need adaptation to specific exhibits.
- **Completion clarity vs. interruption:** Visitors should understand when a sequence is complete, but the end state should not abruptly break the museum flow.

---

## Solution

Divide the exhibit explanation into a sequence of manageable content units. Each unit should present one focused idea, such as a body part, historical fact, behavioural mechanism, ecological relation, or interpretive theme.

Provide a clear navigation interface that allows visitors to move forward and backward through the sequence. The interface should include **Previous** and **Next** controls, and may include a step count, progress bar, title, category label, or lightweight state indicator. Visitors should be able to pause, repeat, skip, exit, or return where appropriate.

Each step may combine text, images, audio narration, animation, 3D models, captions, or spatial highlights, but each medium should serve a distinct interpretive purpose. Avoid presenting all available information simultaneously. Instead, reveal content progressively so that visitors understand what to attend to next.

If the exhibit contains several thematic categories, the system may organize the sequence into a small number of tabs or modules, such as anatomy, habitat, behaviour, or conservation. Within each category, content should remain sequential and easy to revisit.

When the sequence is complete, provide a clear end state. The system may summarize the content, return to an overview, suggest another module, hand over to **AR Labelling**, or return to a guidance pattern for the next point of interest.

---

## Design Parameters and Recommended Settings

- **Content unit length:** Keep each step focused on one main idea or exhibit relation.
- **Number of categories:** Use approximately **3–6 categories** per exhibit when thematic grouping is needed.
- **Number of steps:** Keep the number of steps manageable for short museum visits; avoid long sequences that require extended reading or waiting.
- **Navigation model:** Use sequential navigation as the default, with optional free-jump navigation, milestone-based progression, or guided branching when appropriate.
- **Button size:** Use large and comfortable targets for HMD interaction; as a practical reference, keep buttons at approximately **10 cm or larger** in perceived target size.
- **Navigation controls:** Provide **Previous**, **Next**, and where appropriate **Repeat**, **Skip**, **Pause**, **Resume**, **Exit**, or **Return**.
- **Progress indicator:** Show lightweight progress information, such as **Step 1/4**, a progress bar, or a current-section title.
- **Presentation modality:** Combine text, images, 3D models, spatial highlights, audio narration, captions, animation, or micro-interactions only when each medium adds interpretive value.
- **Spatial anchoring:** Decide whether panels and controls should be exhibit-anchored, body-anchored, environment-anchored, or hybrid. The choice should preserve readability while maintaining connection to the exhibit.
- **Text amount:** Use concise text blocks and avoid dense paragraphs in the HMD field of view.
- **Audio duration:** Keep narration segments short and allow visitors to pause or repeat them.
- **Media control:** For looping animation or video, provide **Pause** and **Resume** controls and define whether media should auto-pause when visitors move to another step.
- **Accessibility settings:** Provide captions or transcripts for audio, adjustable text size and contrast, non-colour-dependent cues, and alternative paths for visitors who cannot use a specific input mode.
- **Exception states:** Define how the system handles skipped steps, paused interaction, off-focus behaviour, low tracking confidence, interrupted media, and exit requests.
- **Telemetry hooks:** Record step entry, step exit, dwell time, navigation direction, skipped content, repeated content, media pause/resume, and completion rate.

---

## Consequences

When applied successfully, Sequential Explanation helps visitors understand complex exhibit information without being overwhelmed. It supports a clear mental model of the content structure, gives visitors control over pacing, and makes it easier to revisit or skip information. It also provides creators with a reusable structure for organizing exhibit content into modular, updateable, and observable content units.

However, the pattern also introduces risks. An overly linear sequence may feel rigid or menu-like, especially for visitors who prefer open exploration. Too many categories or steps can create cognitive load or choice fatigue. Poorly placed panels or controls may distract from the physical exhibit. Time-based media may also trap visitors in a fixed pace if pause, repeat, or skip controls are not provided. The pattern therefore requires careful tuning of content granularity, navigation freedom, progress feedback, media density, and spatial anchoring.

---

## Related Patterns

- **Preceding activation patterns**
  - **Step-In Trigger** can precede Sequential Explanation when visitors should first activate the exhibit experience through a spatial entry zone.
  - **Exhibit Knowledge Trigger** can precede Sequential Explanation when a short concept-linked micro-task should unlock the explanation sequence.

- **Preceding guidance patterns**
  - **Avatar Guide** can indirectly precede Sequential Explanation by guiding visitors to the point of interest before activation and presentation.
  - **Forward Cue-Routing** can indirectly precede Sequential Explanation by guiding visitors through lightweight route cues before activation and presentation.

- **Complementary presentation patterns**
  - **AR Labelling** can complement Sequential Explanation by attaching labels or annotations to exhibit parts within each step.
  - **AR Exhibit Reassembler** can complement or follow Sequential Explanation when visitors should reconstruct missing or fragmented exhibit elements after receiving structured background information.
  - **AR Exhibit Feature Drawing** can complement or follow Sequential Explanation when visitors should draw, trace, or mark features after learning about them.
  - **AR Object Catching** can complement or follow Sequential Explanation when a structured explanation introduces a later embodied or playful task.

---

## Composition Notes

Sequential Explanation normally occupies the main exhibit-centred presentation phase of an HMD-AR museum experience. A typical composition is:

**PoI Guide → Experience Indicator → Sequential Explanation**

For example:

**Avatar Guide → Step-In Trigger → Sequential Explanation → AR Labelling**

The handoff from activation should be clear. Once **Step-In Trigger** or **Exhibit Knowledge Trigger** activates the experience, the Sequential Explanation interface should become visually primary and should communicate the first available action or content unit.

When Sequential Explanation is combined with other presenter patterns, it often defines the primary flow. For example, **AR Labelling** may appear inside individual explanation steps to connect textual or audio explanation to physical exhibit parts. At completion, the system may provide a summary, return to the exhibit overview, suggest another presenter module, or hand back to a guidance pattern for the next point of interest.

---

## Implementation Alignment

The pattern can be implemented as a reusable content-sequencing module or Unity prefab that combines:

- content-unit metadata;
- ordered step logic;
- category or module selection;
- navigation controls;
- progress tracking;
- media playback control;
- panel or spatial UI placement;
- accessibility settings;
- event-based handoff to complementary modules.

Relevant exposed parameters include category list, step order, step title, text entries, images, 3D models, audio clips, video clips, spatial highlight targets, navigation mode, button size, panel placement, anchoring type, progress indicator style, media pause/resume behaviour, captions, text size, contrast settings, completion rules, and fallback behaviour.

Implementation-level events may include:

- sequence started;
- category selected;
- step opened;
- next selected;
- previous selected;
- step repeated;
- step skipped;
- media played;
- media paused;
- media resumed;
- spatial highlight shown;
- step completed;
- sequence completed;
- sequence exited;
- fallback used.

These events can support debugging, system logs, observation sheets, content iteration, and later evaluation of dwell time, skipped content, repeated content, completion rate, navigation errors, and transition success.

---

## Example Use

In a natural-history museum, visitors activate an AR experience at a dinosaur or whale exhibit. The Sequential Explanation interface opens with a first step introducing the exhibit. Visitors then use **Next** and **Previous** controls to move through short explanation panels about anatomy, habitat, behaviour, and ecological adaptation.

Each step may include concise text, audio narration, images, spatial highlights, or a small 3D animation. A lightweight progress indicator shows the current position in the sequence, such as **Step 2/5**. Visitors can pause or repeat audio and continue at their own pace. After the final step, the system may open an **AR Labelling** layer that lets visitors inspect specific exhibit parts in more detail.

<div class="intro-video-wrapper">
  <iframe
    src="https://www.youtube-nocookie.com/embed/ukEJim45PAE"
    title="YouTube video player"
    frameborder="0"
    allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture"
    allowfullscreen
  ></iframe>
</div>