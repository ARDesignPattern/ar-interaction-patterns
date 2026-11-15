---
layout: tech
title: AR Labelling
order: 4
description: Spatially associated digital labels for presenting contextual information about museum exhibits.
image: /images/TechImage/DigitalLabel.png
tech_category: presenter
github: https://github.com/ARDesignPattern/AR-Design-Patterns_Git/releases/tag/DigitalLabel_v1.0.0
download: https://github.com/ARDesignPattern/AR-Design-Patterns_Git/releases/tag/DigitalLabel_v1.0.0
---

<div class="tech-detail">

  <header class="tech-detail-header">
    <p class="tech-eyebrow">
      APPLICATION-LEVEL IMPLEMENTATION / EXPERIENCE PRESENTER
    </p>

    <h1 class="page-title">{{ page.title }}</h1>

    <p class="tech-implementation-name">
      Unity Implementation: <strong>Digital Label</strong>
    </p>

    <p class="tech-lead">{{ page.description }}</p>

  </header>

  <div class="image-wrapper">
    <img
      src="{{ page.image | relative_url }}"
      alt="AR Labelling – Digital Label Unity implementation"
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
        <h3>Contextual Labels</h3>
        <p>
          Presents digital titles and descriptive information
          associated with museum exhibits.
        </p>
      </div>

      <div class="tech-feature">
        <h3>Spatial Association</h3>
        <p>
          Uses a visual connector to establish the relationship
          between a label and its target object.
        </p>
      </div>

      <div class="tech-feature">
        <h3>Customizable Content</h3>
        <p>
          Supports replacing demonstration text and objects
          with exhibition-specific information.
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
        Open the example scene or add the Digital Label
        prefab to your scene.
      </li>
      <li>
        Replace the demonstration labels and objects,
        then configure spatial positioning and
        target references in the Unity Inspector.
      </li>
    </ol>

    <p class="tech-note">
      Basic Unity knowledge is assumed.
      Application-specific label content, spatial layout,
      and parameter tuning remain the responsibility
      of the Author User.
    </p>

  </section>

  <section class="tech-block">
    <h2>Implementation Resources</h2>

    <div class="tech-resource-panel">

      <div class="tech-resource-info">
        <strong>Digital Label</strong>
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
        AR Labelling
      </a>
    </p>

  </section>

</div>
