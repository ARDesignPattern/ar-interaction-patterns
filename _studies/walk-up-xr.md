---
title: "Walk-up XR for Real-World Environments"
---

This research investigates how interaction design for head-mounted augmented reality can support first-time museum visitors and how recurring design solutions can be transformed into reusable design knowledge.

The work developed through a sequence of empirical studies, iterative prototypes, and field deployments, eventually forming a parameterized HMD-AR interaction pattern system.

## 1. HMD-AR introduces interaction problems that cannot simply be inherited from handheld AR

Head-mounted AR creates a different interaction situation from smartphone- and tablet-based AR. Museum visitors must understand spatial interfaces, discover interactive content, coordinate movement and attention, and learn unfamiliar input techniques while simultaneously engaging with physical exhibits.

Early work therefore examined which interaction conventions could be transferred across devices and where HMD-based AR required its own interaction solutions. This established the initial design problem for the doctoral research: creating interaction approaches that remain understandable for first-time users while taking advantage of spatial and head-mounted interaction.

![Visitor interaction loop between navigation and exploration]({{ '/images/studies/walk-up-xr/VisitLoop.jpeg' | relative_url }})

_Conceptual visitor loop used in the early research to describe the recurring transition between navigation toward a point of interest and exploration of AR content at the exhibit._

## 2. A pattern-based research process was used to turn recurring problems into reusable design knowledge

The research subsequently combined Design Science Research (DSR) [1], Research through Design (RtD) [2], and pattern-language principles [3,4] as a structured way of moving between problem identification, design intervention, prototyping, evaluation, and abstraction.

Within this process, prototypes were not treated only as final applications. They acted as research artifacts through which interaction ideas could be instantiated, tested, compared, and progressively generalized. Recurring solutions and design decisions were then documented as patterns and parameters that could be reused across museum AR situations.

This process eventually provided the methodological basis for developing a coherent HMD-AR interaction pattern system rather than a collection of unrelated interface solutions.

![Combined RtD × DSR framework used in the dissertation.]({{ '/images/studies/walk-up-xr/RSD_DSR.jpeg' | relative_url }})

_Combined RtD × DSR framework used in the dissertation. DSR structures the overall research backbone [1], while the four research phases organize the empirical and design work. RtD operates as a shared iterative inquiry cycle across these phases [2], generating evidence that is progressively abstracted into reusable design knowledge. Pattern-language principles support the documentation of recurring problems and reusable solution structures as interconnected design knowledge [3,4]._

### References

[1] Hevner, A. R., March, S. T., Park, J., & Ram, S. (2004). _Design science in information systems research._ MIS Quarterly, 28(1), 75–105. DOI: 10.2307/25148625.

[2] Zimmerman, J., Forlizzi, J., & Evenson, S. (2007). _Research through design as a method for interaction design research in HCI._ Proceedings of the SIGCHI Conference on Human Factors in Computing Systems (CHI '07), 493–502. DOI: 10.1145/1240624.1240704.

[3] Alexander, C., Ishikawa, S., & Silverstein, M. (1977). _A Pattern Language: Towns, Buildings, Construction._ Oxford University Press.

[4] Borchers, J. (2001). _A Pattern Approach to Interaction Design._ John Wiley & Sons.

### Related research

- [A Pattern Language for Head-Mounted AR in Museums: Parameterized, Composable, and Reproducible](https://yuliu.design/ar-interaction-patterns/literature.html#pattern-language-hmd-ar-museums)

## 3. Interaction concepts were iteratively developed and tested in realistic museum situations

A series of prototypes and user studies investigated how first-time visitors actually encounter HMD-based AR in exhibition environments.

The studies first identified interaction difficulties experienced by novice HMD users and explored ways of supporting onboarding and omnidirectional guidance. Subsequent prototypes extended this work toward spatial and locative interaction, playful visitor movement, and game-mechanic-based experiences.

Across these iterations, the research examined practical questions such as how visitors discover AR content, understand where to move, interpret spatial cues, manipulate virtual content, and remain engaged with both digital experiences and physical exhibits.

Testing in museum-oriented and real-world settings allowed interaction concepts to be refined under conditions closer to their intended use rather than relying only on laboratory demonstrations.

![Whale exhibit HMD-AR prototype]({{ '/images/studies/walk-up-xr/Whale%20Exhibit.jpg' | relative_url }})

_An early museum HMD-AR prototype developed around a large whale exhibit. The experience explored how spatially registered digital content, visual guidance, and exhibit-linked interaction could support visitor attention around a large physical object. [View project ↗](https://yuliu.design/projects/whale-exhibition/)_

![Triceratops HMD-AR interaction prototype]({{ '/images/studies/walk-up-xr/Triceratops.jpg' | relative_url }})

_A Triceratops-based prototype combining guided explanation with an interactive reconstruction task. Visitors first encountered explanatory AR content and then manipulated virtual skeletal elements as part of a puzzle-like museum experience. [View project ↗](https://yuliu.design/projects/triceratops-exhibition/)_

![Deinonychus HMD-AR interaction prototype]({{ '/images/studies/walk-up-xr/Deinonychus.jpg' | relative_url }})

_A Deinonychus prototype used to investigate direct interaction with virtual content placed around a physical exhibit. The study explored how first-time HMD users interpret spatial cues, select virtual elements, and act within an exhibit-centered interaction space. [View project ↗](https://yuliu.design/projects/deinonychus-exhibition/)_

![Coral Reef HMD-AR interaction prototype]({{ '/images/studies/walk-up-xr/Coral%20Reef.jpg' | relative_url }})

_A coral-reef prototype extending the research toward more exploratory and playful forms of museum interaction. It combined spatial guidance, interactive virtual objects, and game-oriented actions to examine how visitors move between physical exhibits and augmented content. [View project ↗](https://yuliu.design/projects/coral-reef-exhibition/)_

![Monk Seal HMD-AR museum prototype]({{ '/images/studies/walk-up-xr/Monk%20Seal.jpg' | relative_url }})

_A field-oriented HMD-AR prototype developed for the monk seal exhibition at the Natural History Museum of Funchal. It brought together spatial guidance, interactive storytelling, and exhibit-related learning in a more complete museum experience deployed under realistic visitor conditions. [View project ↗](https://yuliu.design/projects/monk-seal-exhibition/)_

### Related research

- [Evaluating Interaction Challenges of Head-Mounted Device-based Augmented Reality Applications for First-time Users at Museums and Exhibitions](https://yuliu.design/ar-interaction-patterns/literature.html#interaction-challenges-first-time-hmd-ar-users)
- [Newbie Guides for Omnidirectional Guidance in Head-Mounted-Device-Based Museum Applications](https://yuliu.design/ar-interaction-patterns/literature.html#newbie-guides-omnidirectional-guidance)
- [Playful Locative Interaction in Museums and Exhibitions with Immersive Augmented Reality](https://yuliu.design/ar-interaction-patterns/literature.html#playful-locative-interaction-museums)
- [Design Patterns for Playful Augmented Reality: Enhancing Cultural Heritage Engagement with Game Mechanics](https://yuliu.design/ar-interaction-patterns/literature.html#playful-ar-design-patterns-cultural-heritage)

## 4. Findings from multiple prototypes were synthesized into a parameterized two-level pattern system

As interaction solutions were repeatedly instantiated and evaluated across different prototypes, the research moved from individual design cases toward abstraction.

Recurring interaction structures were synthesized into reusable design knowledge that could be adapted to different exhibits and visitor situations. Rather than defining patterns as fixed interface recipes, the system incorporates explicit parameters that allow designers to adjust aspects such as activation, spatial placement, presentation, and interaction behavior.

The resulting system distinguishes between higher-level pattern classes and more concrete application-level patterns. This two-level organization supports both reuse and adaptation: broader structures describe recurring interaction purposes, while application-level patterns provide more directly implementable solutions.

Empirical studies across different prototype configurations provided evidence for refining these patterns and their parameters, while also identifying where design decisions remained dependent on context.

![Consolidated two-level HMD-AR interaction pattern system]({{ '/images/studies/walk-up-xr/PatternSystem.jpeg' | relative_url }})

_The research iterations were progressively consolidated into a two-level interaction pattern system connecting the visitor journey with category-level and application-level design patterns. The resulting structure captures recurring interaction problems, reusable solution strategies, and configurable design knowledge derived from the prototype and field-study process. [Explore the pattern system ↗]({{ '/patterns/' | relative_url }})_

### Related research

- [Parameterized Head-Mounted Augmented Reality Design Patterns for Cultural Heritage: An Empirical Study](https://yuliu.design/ar-interaction-patterns/literature.html#parameterized-hmd-ar-design-patterns)
- [A Pattern Language for Head-Mounted AR in Museums: Parameterized, Composable, and Reproducible](https://yuliu.design/ar-interaction-patterns/literature.html#pattern-language-hmd-ar-museums)

## 5. The pattern system was validated through multiple complementary forms of evidence

The resulting pattern system was evaluated from both visitor-side and creator-side perspectives. Creator and expert evaluation examined whether the patterns could be understood, interpreted, and reused as design knowledge, while visitor studies investigated whether pattern-based implementations could support feasible, usable, and engaging HMD-AR experiences under museum conditions.

Visitor-side validation was conducted across multiple museum prototypes and deployment contexts. In particular, the Whale Exhibit and Monk Seal experiences provided evidence across different exhibits and sites, allowing the research to examine whether a stable interaction-layer composition could be transferred and reconfigured while maintaining comparable experience outcomes. These evaluations covered multiple dimensions of visitor experience, including usability, cognitive load, immersion, and playfulness.

The validation was therefore not limited to the success of a single prototype. Cross-site comparison provided additional evidence that the underlying interaction structure could remain stable while content, exhibit characteristics, and contextual parameters were adapted to different museum settings.

Beyond system-level evaluation, focused parameter studies examined specific design decisions represented within the pattern system. One example is UI placement and semantic anchoring: whether interface elements should be attached to the visitor, positioned relative to the physical exhibit, or configured according to the interaction context. These studies provided more detailed empirical evidence about individual design parameters and the trade-offs they introduce.

Taken together, the creator-side evaluation, visitor studies, cross-site validation, and focused parameter studies provided converging positive evidence for the usability, adaptability, and reusability of the pattern system as design knowledge for HMD-AR museum experiences.

### Related research

- [A Pattern Language for Head-Mounted AR in Museums: Parameterized, Composable, and Reproducible](https://yuliu.design/ar-interaction-patterns/literature.html#pattern-language-hmd-ar-museums)

- [Parameterized Head-Mounted Augmented Reality Design Patterns for Cultural Heritage: An Empirical Study](https://yuliu.design/ar-interaction-patterns/literature.html#parameterized-hmd-ar-design-patterns)

- [Semantic Anchoring in Head-Mounted Display-based Museum Augmented Reality: A Mixed-Methods Study of User Interface Placement and Experience](https://yuliu.design/ar-interaction-patterns/literature.html#semantic-anchoring-hmd-ar)
