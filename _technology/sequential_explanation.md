---
layout: tech
title: Sequential Explanation
order: 3
description: Step-by-step presentation of narrative content through interactive AR controls.
image: /images/TechImage/Sequential.png
tech_category: presenter
github: https://github.com/ARDesignPattern/AR-Design-Patterns_Git/releases/tag/SequentialExplanation_v1.0.1
download: https://github.com/ARDesignPattern/AR-Design-Patterns_Git/releases/tag/SequentialExplanation_v1.0.1
---

<div class="tech-detail">

  <header class="tech-detail-header">
    <p class="tech-eyebrow">
      APPLICATION-LEVEL IMPLEMENTATION / EXPERIENCE PRESENTER
    </p>

    <h1 class="page-title">{{ page.title }}</h1>

    <p class="tech-implementation-name">
      Unity Implementation:
      <strong>Sequential Explanation</strong>
    </p>

    <p class="tech-lead">{{ page.description }}</p>

  </header>

  <div class="image-wrapper">
    <img
      src="{{ page.image | relative_url }}"
      alt="Sequential Explanation Unity implementation"
      class="tech-image">
  </div>

  <div class="tech-specs">
    <span>Unity 2020.3.25f1</span>
    <span>MRTK 2.8.3</span>
    <span>URP 10.7.0</span>
    <span>HoloLens 2</span>
  </div>

  <section class="tech-block">
    <h2>Interaction Features</h2>

    <div class="tech-feature-grid">

      <div class="tech-feature">
        <h3>Sequential Narrative</h3>
        <p>
          Presents exhibition information in a structured,
          step-by-step sequence.
        </p>
      </div>

      <div class="tech-feature">
        <h3>Interactive Navigation</h3>
        <p>
          Allows visitors to move between narrative stages
          using Previous and Next controls.
        </p>
      </div>

      <div class="tech-feature">
        <h3>Content Integration</h3>
        <p>
          Supports replacing demonstration content with
          exhibition-specific text and visual assets.
        </p>
      </div>

    </div>

  </section>

  <section class="tech-block">
    <h2>Quick Start</h2>

    <ol class="tech-steps">
      <li>
        Import the UnityPackage into a compatible Unity project.
      </li>
      <li>
        Open the example scene or add the Sequential
        Explanation prefab to your scene.
      </li>
      <li>
        Replace the demonstration content and configure
        narrative stages and interaction references
        in the Unity Inspector.
      </li>
    </ol>

    <p class="tech-note">
      Basic Unity knowledge is assumed.
      Application-specific narrative design, parameter tuning,
      and scene composition remain the responsibility
      of the Author User.
    </p>

  </section>

  <section class="tech-block">
    <h2>Implementation Resources</h2>

    <div class="tech-resource-panel">

      <div class="tech-resource-info">
        <strong>Sequential Explanation</strong>
        <span>UnityPackage · v1.0.1</span>
      </div>

      <div class="tech-actions">
        <a
          href="{{ page.github }}"
          class="tech-secondary-button"
          target="_blank"
          rel="noopener noreferrer">
          GitHub Details
        </a>

        <a
          href="{{ page.download }}"
          class="tech-primary-button"
          target="_blank"
          rel="noopener noreferrer">
          Download Package
        </a>
      </div>

    </div>

    <p class="tech-related">
      Related Design Pattern:
      <a href="{{ '/patterns.html' | relative_url }}">
        Sequential Explanation
      </a>
    </p>

  </section>

</div>
