# Research Problem Definition: Environmental Audio Reasoning (EAR)

## 1. Problem Formulation

The core research task of this project is formalized as follows:

Given a visual observation $V$ (which may be a static image $I_s$ or a short video sequence $V_d$), infer a set of latent environmental, physical, and acoustic descriptors $L_{acoustic}$, and use them to synthesize a realistic, spatialized multi-channel audio stream $A$ that matches the physical context of the scene.

$$\text{Visual Input } (V) \longrightarrow \text{Latent Acoustic Model } (L_{acoustic}) \longrightarrow \text{Spatialized Audio Output } (A)$$

---

## 2. In-Scope vs. Out-of-Scope Problems

To maintain research focus, we define clear boundaries:

### What Is the Problem (In-Scope)
*   **Physical Property Estimation**: Inferring material composition, surface hardness, geometry, and spatial dimensions from visual characteristics.
*   **Sound Source Identification**: Determining which visual objects are active resonators (e.g., a running waterfall, a passing car) or passive resonators (e.g., a wall reflecting sound).
*   **Commonsense Event Association**: Inferring temporal actions that are not explicitly visible (e.g., wind rustling palm leaves, footsteps on sand) based on contextual clues (e.g., trees bending, footprints in sand).
*   **Acoustic Simulation**: Modeling how sound waves propagate from identified sources to a hypothetical listener within the visual geometry.

### What Is NOT the Problem (Out-of-Scope)
*   **High-fidelity Raw Synthesis**: Improving the state of the art in raw neural audio codecs or waveform generation (we will leverage existing architectures like AudioCraft, AudioLDM, or Vocoders).
*   **Musical Composition**: Generating soundtracks, background scores, or stylized musical accompaniment for images.
*   **Direct Translation (Black-box)**: Training end-to-end models that map pixels directly to raw wave files without intermediate reasoning.
*   **Arbitrary Text-to-Audio**: Building models that generate sounds from textual descriptions alone (e.g., "generate rain sound"), unless the text is derived directly from visual reasoning steps.

---

## 3. Core Scientific Assumptions

The project is built on the following assumptions:

1.  **Visual Latency of Sound**: Visual characteristics of objects and environments contain latent clues about their physical dynamics and material properties (e.g., texture reveals surface roughness, position reveals spatial relationships).

## Open Questions
*   How do we handle the computational cost of simulating wave-based acoustic propagation in real-time?


## Related Documents

*   [Project Overview](00_Project_Overview.md)
*   [Project Vision](01_Project_Vision.md)
*   [Project Principles](04_Project_Principles.md)
