---
layout: tech
title: Avatar Guide
order: 5
description: Virtual avatar guidance using predefined navigation paths for HMD-AR museum experiences.
image: /images/TechImage/AvatarGuide.png
tech_category: guidance
github: https://github.com/ARDesignPattern/AR-Design-Patterns_Git/releases/tag/GuideAvatar_v1.0.1
download: https://github.com/ARDesignPattern/AR-Design-Patterns_Git/releases/tag/GuideAvatar_v1.0.1
---

<div class="tech-detail">

  <header class="tech-detail-header">
    <p class="tech-eyebrow">
      APPLICATION-LEVEL IMPLEMENTATION / POINT OF INTEREST GUIDE
    </p>

    <h1 class="page-title">{{ page.title }}</h1>

    <p class="tech-implementation-name">
      Unity Implementation: <strong>Guide Avatar</strong>
    </p>

    <p class="tech-lead">{{ page.description }}</p>

  </header>

  <div class="image-wrapper">
    <img
      src="{{ page.image | relative_url }}"
      alt="Avatar Guide – Guide Avatar Unity implementation"
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
        <h3>Virtual Guide</h3>
        <p>
          Provides a virtual avatar to support visitor
          orientation and spatial guidance.
        </p>
      </div>

      <div class="tech-feature">
        <h3>Path-Based Navigation</h3>
        <p>
          Loads predefined navigation paths from JSON data
          to guide the avatar along specified routes.
        </p>
      </div>

      <div class="tech-feature">
        <h3>Playback Control</h3>
        <p>
          Provides controls for starting, pausing,
          resuming, and resetting guided navigation.
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
        Open the example scene or add the Guide Avatar
        prefab to your scene.
      </li>
      <li>
        Replace demonstration objects, configure the
        navigation path data, and reconnect the required
        GameObject references in the Unity Inspector.
      </li>
    </ol>

    <p class="tech-note">
      Navigation data is loaded from
      <code>Resources/paths.json</code>.
      Basic Unity knowledge is assumed.
      Application-specific routes, waypoint coordinates,
      spatial alignment, and parameter tuning remain
      the responsibility of the Author User.
    </p>

  </section>

  <section class="tech-block">
    <h2>Implementation Resources</h2>

    <div class="tech-resource-panel">

      <div class="tech-resource-info">
        <strong>Guide Avatar</strong>
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
        Avatar Guide
      </a>
    </p>

  </section>

</div>
