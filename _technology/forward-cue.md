---
layout: tech
title: Forward Cue–Routing
order: 1
description: Floor-based directional guidance using animated visual cues and spatial audio for HMD-AR navigation.
image: /images/TechImage/ForwardCueRootImage.png
tech_category: guidance
github: https://github.com/ARDesignPattern/AR-Design-Patterns_Git/releases/tag/ForwardCue_Routing_v1.0
download: https://github.com/ARDesignPattern/AR-Design-Patterns_Git/releases/download/ForwardCue_Routing_v1.0/ForwardCue_Routing.unitypackage
---

<div class="tech-detail">

  <header class="tech-detail-header">
    <p class="tech-eyebrow">
      APPLICATION-LEVEL IMPLEMENTATION / POINT OF INTEREST GUIDE
    </p>

    <h1 class="page-title">{{ page.title }}</h1>

    <p class="tech-implementation-name">
      Unity Implementation: <strong>Forward Cue Root</strong>
    </p>

    <p class="tech-lead">{{ page.description }}</p>

  </header>

  <div class="image-wrapper">
    <img
      src="{{ page.image | relative_url }}"
      alt="Forward Cue–Routing Unity implementation"
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
        <h3>Directional Cues</h3>
        <p>
          Animated floor-based ripple cues indicate the intended
          navigation direction.
        </p>
      </div>

      <div class="tech-feature">
        <h3>Route Guidance</h3>
        <p>
          Supports navigation along predefined routes and
          toward selected points of interest.
        </p>
      </div>

      <div class="tech-feature">
        <h3>Spatial Feedback</h3>
        <p>
          Combines visual transitions and localized audio cues
          to support spatial orientation.
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
        Open the example scene or add the Forward Cue prefab
        to your existing scene.
      </li>
      <li>
        Locate the navigation GameObjects in the Unity Hierarchy,
        replace demonstration objects, and configure route
        references and interaction events in the Inspector.
      </li>
    </ol>

    <p class="tech-note">
      Basic Unity knowledge is assumed. Application-specific
      navigation paths, parameter tuning, content integration,
      and scene design are the responsibility of the Author User.
    </p>

  </section>

  <section class="tech-block">
    <h2>Implementation Resources</h2>

    <div class="tech-resource-panel">

      <div class="tech-resource-info">
        <strong>Forward Cue Root</strong>
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
        Forward Cue–Routing
      </a>
    </p>

  </section>

</div>
