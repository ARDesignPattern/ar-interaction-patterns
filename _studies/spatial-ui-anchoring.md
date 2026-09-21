---
title: "Empirical Validation of HMD-AR Interaction Design"

study_number: "05"

subtitle: "Validating a reusable HMD-AR pattern system and examining the experiential effects of specific design parameters."

tags:
  - "Empirical Validation"
  - "Design Parameters"
  - "Museum XR"
---

This study examines how the HMD-AR interaction pattern system was empirically validated and how individual design parameters were subsequently investigated in greater depth.

Validation was conducted at two complementary levels. First, the pattern system itself was evaluated from both visitor and creator perspectives. Second, selected design parameters were examined through focused comparative studies to understand how alternative configurations influence interaction behavior and visitor experience.

## 1. Validating the pattern system from visitor and creator perspectives

The pattern system was designed for two different groups of users.

The first group consists of **museum visitors**, because the interaction designs ultimately need to support usable, understandable, and engaging visitor experiences.

The second group consists of **creators**, because the patterns are intended to function as reusable design knowledge for developing new HMD-AR museum experiences. Since museum XR is inherently interdisciplinary, the creator-side evaluation included two complementary forms of expertise: **AR developers**, who contribute technical and interaction-design knowledge, and **cultural heritage creators**, who contribute expertise in interpretation, exhibition content, storytelling, and visitor communication.

The validation therefore combined visitor-side and creator-side evidence rather than relying on a single prototype evaluation.

### Visitor-side validation across two museum contexts

Visitor-side evaluation combined quantitative and qualitative methods. The methodological approach followed the field-evaluation framework described in [Evaluating HMD Interaction in Museums]({{ '/studies/xr-evaluation-museums/' | relative_url }}), combining standardized experience measures with observation and qualitative feedback.

Pattern-based prototypes were evaluated in two different real-world museum contexts: the [Senckenberg Naturmuseum Frankfurt](https://museumfrankfurt.senckenberg.de/en/) in Germany and the [Natural History Museum of Funchal](https://visitmadeira.com/en/what-to-do/culture-passionates/heritage/museums/natural-history-museum-of-funchal/) in Madeira, Portugal.

The Frankfurt deployment was developed around the whale exhibition, while the Funchal deployment adapted related interaction structures to the monk seal exhibition. Although the exhibit content, spatial conditions, and narrative context differed, the underlying interaction-layer composition was retained and reconfigured through pattern parameters.

![Pattern-based HMD-AR experience at the whale exhibition in Frankfurt]({{ '/images/studies/Validation/WhaleExhibit.jpeg' | relative_url }})

_Pattern-based HMD-AR experience evaluated around the whale exhibit at the Senckenberg Naturmuseum Frankfurt._

![Pattern-based HMD-AR experience at the monk seal exhibition in Funchal]({{ '/images/studies/Validation/MonkSealExhibit.jpeg' | relative_url }})

_Adapted HMD-AR experience evaluated at the Natural History Museum of Funchal, demonstrating how a related interaction structure could be reconfigured for a different exhibit and museum context._

The quantitative evaluations considered multiple dimensions of visitor experience, including usability, perceived workload, spatial presence, and playfulness. Across the two deployments, the outcomes remained within positive or acceptable ranges, and the overall experience profiles were broadly consistent across the different museum contexts.
A mixed-methods field study compared two configurations
![Feasibility and acceptability outcomes across visitor evaluations]({{ '/images/studies/Validation/feasibilityAndAcceptabilityOutcomes.jpeg' | relative_url }})

_Overview of visitor-side feasibility and acceptability outcomes. Measures including SUS, NASA-TLX, spatial-presence measures, and GAMEFULQUEST showed broadly consistent and acceptable experience profiles across the evaluated deployments._

These results do not imply that the two museum experiences were identical. Rather, they provide evidence that a stable interaction-layer composition could be adapted to substantially different exhibits while maintaining a comparable visitor-side outcome profile.

### Creator-side validation

The creator-side evaluation examined whether the pattern system could be understood and used as design knowledge by people with different professional backgrounds.

Ten expert participants took part in this evaluation: five with an AR development perspective and five with a cultural heritage content-creation perspective. This distinction was important because the pattern system is intended to operate across technical, interaction-design, and cultural-interpretation concerns rather than serving only one professional group.

The experts assessed the patterns using a four-level evaluation procedure. Their judgments were analyzed through a content-validity approach to determine whether individual patterns were consistently regarded as relevant and appropriate across the different expert perspectives.

![Content-validity assessment of the pattern system]({{ '/images/studies/Validation/ContentValidityPassMatrix.jpeg' | relative_url }})

_Content-validity assessment across AR-development and cultural-heritage creator perspectives. The evaluation showed broad agreement on the relevance and applicability of the pattern system across the two expert groups._

Taken together, the visitor-side studies and creator-side evaluation provided complementary evidence for the pattern system. Visitor studies examined whether pattern-based implementations could support feasible and positively received museum experiences, while expert evaluation examined whether the system itself could function as understandable and reusable design knowledge for interdisciplinary creators.

### Related research

- [A Pattern Language for Head-Mounted AR in Museums: Parameterized, Composable, and Reproducible](https://yuliu.design/ar-interaction-patterns/literature.html#pattern-language-hmd-ar-museums)

## 2. Validating specific parameters through comparative design configurations

After the broader pattern system had been established, subsequent research examined individual design parameters in greater depth.

Rather than starting from a completely new interaction concept, these studies used the pattern-based design structure as a stable foundation and varied specific parameters within that structure. This made it possible to investigate how alternative design configurations influence the resulting visitor experience.

One such parameter was **semantic anchoring**: where interface controls are positioned in relation to the visitor and the physical exhibit.

A mixed-methods field study compared two configurations of the same museum AR experience. One version used **body-anchored controls**, attaching interaction elements to the visitor, while the other used **exhibit-anchored controls**, positioning them in relation to the physical artefact.

![Comparison of exhibit-anchored and body-anchored UI placement]({{ '/images/studies/Validation/UIplacement.jpeg' | relative_url }})

_Comparison of the two UI-placement configurations examined in the semantic-anchoring study. The exhibit-anchored version positioned controls in relation to the physical artefact, while the body-anchored version attached controls to the visitor._

The comparison examined usability, cognitive load, spatial presence, playful or gameful experience, observable interaction behavior, and qualitative visitor feedback.

Both configurations produced usable and acceptable experiences, but they generated different experiential profiles.

The body-anchored configuration was associated with stronger playful/game-related experience and spatial presence, together with more visitor-initiated interaction and movement around the exhibit. The exhibit-anchored configuration produced higher usability ratings and more exhibit-centered, comparatively stationary interaction. Cognitive-load outcomes remained similar across the two versions.

![Visitor outcomes across body-anchored and exhibit-anchored configurations]({{ '/images/studies/Validation/OutcomesAcrossTwoVersions.jpeg' | relative_url }})

_Comparison of visitor outcomes across the two anchoring configurations. The results illustrate a design trade-off rather than a universally preferable placement strategy: body anchoring supported stronger interaction initiative and experiential engagement, while exhibit anchoring emphasized usability and a closer semantic relationship between controls and the physical artefact._

The qualitative observations reinforced this interpretation. Body-anchored controls encouraged visitors to initiate actions and move more actively through the interaction space, whereas exhibit-anchored controls foregrounded the artefact and supported a more observational interaction style.

These findings demonstrate why design parameters should not be treated as minor implementation details. Changing a single parameter within an otherwise related interaction structure can alter how visitors move, attend to the exhibit, initiate actions, and experience the AR content.

Parameter-level validation therefore complements the broader validation of the pattern system. The pattern language provides reusable design structures, while focused empirical studies provide evidence about the consequences and trade-offs associated with particular parameter choices.

### Related research

- [Semantic Anchoring in Head-Mounted Display-based Museum Augmented Reality: A Mixed-Methods Study of User Interface Placement and Experience](https://yuliu.design/ar-interaction-patterns/literature.html#semantic-anchoring-hmd-ar)
