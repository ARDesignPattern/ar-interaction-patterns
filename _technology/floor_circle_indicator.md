---
layout: tech
title: Step-In Trigger
order: 2
description: Floor-based proximity activation for HMD-AR exhibition experiences.
image: /images/TechImage/FloorCircle_Indicator.png
tech_category: indicator
github: https://github.com/ARDesignPattern/AR-Design-Patterns_Git/releases/tag/floor_circle_indicator_v1.0
download: https://github.com/ARDesignPattern/AR-Design-Patterns_Git/releases/download/floor_circle_indicator_v1.0/FloorCircle_Indicator.unitypackage
---

<div class="tech-detail">

  <header class="tech-detail-header">
    <p class="tech-eyebrow">
      APPLICATION-LEVEL IMPLEMENTATION / EXPERIENCE INDICATOR
    </p>

    <h1 class="page-title">{{ page.title }}</h1>

    <p class="tech-implementation-name">
      Unity Implementation: <strong>Floor Circle Indicator</strong>
    </p>

    <p class="tech-lead">{{ page.description }}</p>

  </header>

  <div class="image-wrapper">
    <img
      src="{{ page.image | relative_url }}"
      alt="Step-In Trigger – Floor Circle Indicator Unity implementation"
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
        <h3>Spatial Cue</h3>
        <p>
          Visual floor indicator marking a spatial interaction zone.
        </p>
      </div>

      <div class="tech-feature">
        <h3>Proximity Trigger</h3>
        <p>
          Activates an interaction when the user enters the defined area.
        </p>
      </div>

      <div class="tech-feature">
        <h3>Multimodal Feedback</h3>
        <p>
          Supports visual animation and audio feedback upon activation.
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
        Open the example scene or add the supplied Prefab to your scene.
      </li>
      <li>
        Replace demonstration objects and configure trigger references
        in the Unity Inspector.
      </li>
    </ol>

    <p class="tech-note">
      Basic Unity knowledge is assumed. Application-specific parameter
      tuning, content integration, and scene design are the
      responsibility of the Author User.
    </p>

  </section>

  <section class="tech-block">
    <h2>Implementation Resources</h2>

    <div class="tech-resource-panel">

      <div class="tech-resource-info">
        <strong>Floor Circle Indicator</strong>
        <span>UnityPackage · v1.0</span>
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
          class="tech-primary-button">
          Download Package
        </a>

      </div>
    </div>

    <p class="tech-related">
      Related Design Pattern:
      <a href="{{ '/patterns.html' | relative_url }}">
        Step-In Trigger
      </a>
    </p>

  </section>

</div>
