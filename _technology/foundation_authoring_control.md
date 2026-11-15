---
layout: tech
title: Foundation – Authoring Control
order: 0
description: A reusable authoring interface for spatial scanning, interaction control, and AR pattern integration.
image: /images/TechImage/AuthoringControl.png
tech_category: authoring
github: https://github.com/ARDesignPattern/AR-Design-Patterns_Git/releases/tag/Foundation_AuthoringControl_v1.0.0
download: https://github.com/ARDesignPattern/AR-Design-Patterns_Git/releases/download/Foundation_AuthoringControl_v1.0.0/00_Foundation_AuthoringControl.unitypackage
---

<div class="tech-detail">

  <header class="tech-detail-header">

    <p class="tech-eyebrow">
      FOUNDATION MODULE / AUTHORING TOOLS
    </p>

    <h1 class="page-title">{{ page.title }}</h1>

    <p class="tech-implementation-name">
      Unity Implementation: <strong>Authoring Control</strong>
    </p>

    <p class="tech-lead">{{ page.description }}</p>

  </header>

  <div class="image-wrapper">
    <img
      src="{{ page.image | relative_url }}"
      alt="Foundation Authoring Control Unity interface"
      class="tech-image">
  </div>

  <div class="tech-specs">
    <span>Unity 2020.3.25f1</span>
    <span>MRTK 2.8.3</span>
    <span>URP 10.7.0</span>
    <span>HoloLens 2</span>
  </div>

  <section class="tech-block">
    <h2>Authoring Features</h2>

    <div class="tech-feature-grid">

      <div class="tech-feature">
        <h3>Spatial Scanning</h3>
        <p>
          Controls the scanning of the physical environment
          during AR authoring and testing.
        </p>
      </div>

      <div class="tech-feature">
        <h3>Interaction Control</h3>
        <p>
          Provides an interface for starting and stopping
          AR interaction patterns.
        </p>
      </div>

      <div class="tech-feature">
        <h3>Pattern Integration</h3>
        <p>
          Allows Author Users to connect the control interface
          to different AR interaction implementations.
        </p>
      </div>

    </div>

  </section>

  <section class="tech-block">
    <h2>Quick Start</h2>

    <ol class="tech-steps">

      <li>
        Import the UnityPackage into a compatible Unity project
        with MRTK and URP configured.
      </li>

      <li>
        Open the included AuthoringControl example scene
        or add the relevant Prefab to your own scene.
      </li>

      <li>
        Locate the control GameObjects in the Unity Hierarchy
        and reconnect the required component references
        and interaction events to your selected patterns.
      </li>

    </ol>

    <p class="tech-note">
      This module is intended for Author Users rather than
      museum visitors. Basic Unity knowledge is assumed.
      Application-specific parameter tuning, scene composition,
      and integration remain the responsibility of the Author User.
    </p>

  </section>

  <section class="tech-block">
    <h2>Implementation Resources</h2>

    <div class="tech-resource-panel">

      <div class="tech-resource-info">
        <strong>Foundation – Authoring Control</strong>
        <span>UnityPackage · v1.0.0</span>
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
      <strong>Module Type:</strong>
      Authoring and debugging support module.
      Not an Application-Level Design Pattern.
    </p>

  </section>

</div>
