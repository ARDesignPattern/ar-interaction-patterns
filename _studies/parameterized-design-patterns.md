---
title: "A Composable Two-Level Pattern System for Museum XR"

study_number: "04"

subtitle: "Structuring reusable interaction design knowledge through parameterized and composable patterns."

tags:
  - "Design Patterns"
  - "Authoring"
  - "Reusable Design Knowledge"
---

This study investigates how recurring interaction solutions from HMD-based museum prototypes can be transformed into reusable and composable design knowledge.

The research moved from concrete prototype analysis toward a two-level pattern system for museum XR. It first identified three recurring interaction clusters and their key parameters, then abstracted these into higher-level design patterns, and finally organized them into a composable pattern language that supports reuse, adaptation, and creation across different exhibit contexts.

## 1. Identifying recurring interaction clusters and their key design parameters

The first stage of the research focused on recurring interaction structures that repeatedly appeared across earlier HMD-AR museum prototypes.

Three interaction clusters were identified.

- **Guidance** — interaction solutions that help visitors move toward a target exhibit or point of interest.
- **Indication and activation** — interaction solutions that inform visitors that AR content is available at an exhibit and how this content can be activated.
- **Presentation and exploration** — interaction solutions that allow visitors to access, control, and explore the content associated with an exhibit.

These three clusters capture core stages of the museum AR visitor experience: reaching relevant exhibits, discovering available AR experiences, and interacting with the presented content.

For each interaction cluster, key design parameters were identified. These parameters describe the aspects of an interaction that can be adjusted while preserving the underlying design intention. Examples include how guidance is visually represented, how AR availability is signaled, how activation is triggered, and how content exploration is controlled.

To examine the practical relevance of these parameters, the three interaction clusters were evaluated with expert users in a simulated museum-like setting. These evaluations helped summarize and validate the main parameter choices that influence user experience within each interaction cluster.

![Evaluation of guidance-related interaction patterns]({{ '/images/studies/parameterized-design-patterns/Evaluation_Guidance.jpeg' | relative_url }})

_Evaluation setup for guidance-related interaction patterns. This interaction cluster focuses on helping visitors move toward a target exhibit or point of interest._

![Evaluation of indication- and activation-related interaction patterns]({{ '/images/studies/parameterized-design-patterns/Evaluation_Indication.jpeg' | relative_url }})

_Evaluation setup for indication- and activation-related interaction patterns. This interaction cluster focuses on showing that AR content is available and how visitors can start it._

![Evaluation of presentation- and exploration-related interaction patterns]({{ '/images/studies/parameterized-design-patterns/Evaluation_Presentation.jpeg' | relative_url }})

_Evaluation setup for presentation- and exploration-related interaction patterns. This interaction cluster focuses on how visitors control and explore exhibit-related AR content._

Together, these evaluations provided an empirically grounded understanding of which parameters matter most for different interaction purposes and how they shape usability and interaction experience.

### Related research

- [Parameterized Head-Mounted Augmented Reality Design Patterns for Cultural Heritage: An Empirical Study](https://yuliu.design/ar-interaction-patterns/literature.html#parameterized-hmd-ar-design-patterns)

## 2. From recurring interaction clusters to a two-level pattern system

The three recurring interaction clusters also corresponded to three key stages in the visitor journey. Based on the findings from the first stage and the recurring experience structure observed across multiple design iterations, these clusters were abstracted into three category-level design patterns:

- **Point of Interest Guide**
- **AR Experience Indicator**
- **AR Experience Presenter**

These category-level patterns describe higher-level design intentions and recurring roles within the museum XR experience.

At the same time, nine more concrete design patterns were retained as application-level patterns. These provide more directly usable interaction solutions, including specific implementations, parameters, and reusable authoring logic. Because they can be instantiated more directly in concrete systems — for example as reusable prefabs or pattern-based building blocks — they function as application-level patterns. The corresponding reusable technical resources and Unity prefabs are described in the [Technology resources]({{ '/tech.html' | relative_url }}).

However, concrete interaction solutions alone are not sufficient. The diversity of exhibits, themes, spaces, and curatorial goals means that creators still need to interpret, adapt, and extend these patterns when designing new museum XR experiences.

For this reason, the three category-level patterns provide a higher level of design knowledge. They support creators not only in selecting existing application-level patterns, but also in designing and creating new solutions based on the same interaction logic.

The resulting pattern language therefore contains twelve patterns in total: three category-level patterns and nine application-level patterns. The complete pattern set can be explored in the [Pattern Library]({{ '/patterns.html' | relative_url }}).

Their organization is not only hierarchical, but also relational. The pattern language captures four main relationship types between patterns:

- **Sequential** — patterns can be combined in ordered visitor flows.
- **Alternative** — different patterns can fulfill a similar design role in different ways.
- **Complementary** — multiple patterns can work together within the same experience.
- **Extension logic** — category-level patterns can be extended by new or more specific application-level patterns.

![Relationship logic within the two-level pattern system]({{ '/images/studies/parameterized-design-patterns/PatternRelationship.jpeg' | relative_url }})

_Relationship logic within the two-level pattern system. The pattern language supports sequential, alternative, complementary, and extension relationships between category-level and application-level patterns._

This structure transforms isolated interaction solutions into a broader pattern system that supports both reuse and creation.

### Related research

- [A Pattern Language for Head-Mounted AR in Museums: Parameterized, Composable, and Reproducible](https://yuliu.design/ar-interaction-patterns/literature.html#pattern-language-hmd-ar-museums)

## 3. Composing patterns into complete museum XR experiences

The final step of the research examined how the patterns can be combined in practice to form larger visitor experiences.

Patterns can be composed in different ways. A single category-level pattern may be instantiated multiple times within one experience, or patterns from different categories may be combined across the visitor journey.

For example, a museum AR experience may begin with a **Point of Interest Guide** pattern that brings visitors toward an exhibit, continue with an **AR Experience Indicator** pattern that makes the available experience visible and activates it, and then use one or more **AR Experience Presenter** patterns to support content interaction and exploration.

Within such a sequence, alternative application-level patterns may be chosen depending on the exhibit context. An **Avatar Guide** or **Forward Cue-Routing** pattern can both serve the guidance role, while different presentation patterns can be combined to support explanation, labelling, interaction, or playful engagement.

Patterns can also reappear across an experience. A visitor may encounter multiple guided transitions between different exhibits, repeated activation cues at different locations, or several presentation patterns combined around the same exhibit. The pattern language therefore supports both repeated use and cross-category composition.

![Two-level pattern system for composing museum XR experiences]({{ '/images/studies/parameterized-design-patterns/two_level_pattern_system.jpeg' | relative_url }})

_The two-level pattern system supports the composition of museum XR experiences by connecting category-level patterns with reusable application-level patterns that can be selected, adapted, and combined._

Rather than defining a fixed recipe, the system provides structured design knowledge that helps creators assemble coherent museum XR experiences while remaining flexible across different exhibit settings and design goals.

### Related research

- [A Pattern Language for Head-Mounted AR in Museums: Parameterized, Composable, and Reproducible](https://yuliu.design/ar-interaction-patterns/literature.html#pattern-language-hmd-ar-museums)
