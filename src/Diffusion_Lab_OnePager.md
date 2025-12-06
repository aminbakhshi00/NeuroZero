# Minimal Diffusion Lab  One Page Overview

## Why this lab?
The Minimal Diffusion Lab turns a complex idea—diffusion based generative modeling—into a tangible, instructor ready assignment for any neural network course. Students implement every major component of a DDPM *from scratch* using only NumPy and Matplotlib. By the end, learners not only run a denoiser but also explain the role of noise schedules, time embeddings, and steepest descent optimization. The lab leans into transparency so that even with AI tools at hand, students must still reason about every design choice.

## Key learning outcomes
1. **Data & normalization intuition**  Students build and normalize a 2D spiral, discovering how scale affects initialization and momentum stability.
2. **Noise scheduling & closed form diffusion**  They derive a linear β schedule, implement the $q(x_t\mid x_0)$ sampler, and visualize forward noising.
3. **Noise predicting MLP**  Learners construct a multi layer network, decide on weight scales/momentum, and justify those choices in relation to their dataset.
4. **Steepest descent training**  The lab forces a full batch training loop with EMA tracking, so students must grapple with learning rate tuning without relying on frameworks.
5. **Reverse diffusion reasoning**  Students fill in the DDPM denoising step, study intermediate snapshots, and connect the math to the resulting generative behavior.
6. **Experimental mindset**  Section 7 demands short, evidence backed investigations (noise schedules, capacity changes, sampler tweaks, failure analysis).

## Why it works (even with AI)
* **Intentional gaps:** Every section contains scaffolded TODOs, hints, and reflection prompts that require custom reasoning before code runs. Copying a solution blindly leaves the notebook broken, so students must internalize the ideas to progress.
* **Concept first discussion:** Markdown explanations for scaled time, normalization impact, and momentum emphasize *why* each component exists, helping instructors grade conceptual mastery, not just code output.
* **Reflections & mini reports:** Learners answer short prompts about visualization choices, smoothing behavior, and sampling trajectories. These responses expose shallow understanding immediately.
* **Instructor parity:** The student notebook mirrors the fully solved instructor version, making it easy for professors to assess progress, supply targeted hints, or extend sections (e.g., classifier guidance or cosine schedules).

## Suggested deployment
1. **Assign as a two week module** after students have seen basic autoencoders/VAEs.  
2. **Provide both notebooks**—students start with the scaffolded version while instructors keep the completed solutions.  
3. **Require reflections and experiment write ups** as part of grading; code alone is not sufficient.  
4. **Encourage AI usage with guardrails:** ask students to cite any AI assistance and explain how they verified the output.  
5. **Optional extension ideas:** add cosine β schedules, multi head time embeddings, or CIFAR like datasets to scale difficulty.

## Why professors will love it
* **Turnkey differentiator:** Gives immediate access to a current research topic without relying on heavyweight frameworks.
* **Assessment friendly:** Built in checkpoints (reflections, experiments) let instructors evaluate understanding quickly.
* **Scalable difficulty:** Can be a first exposure to generative models or a launchpad for advanced projects (e.g., classifier free guidance).
* **AI resilient:** The lab’s design compels students to justify choices, ensuring that AI assistance enhances learning rather than replacing it.

**Bottom line:** Minimal Diffusion Lab delivers a modern, high impact assignment that keeps students in the driver’s seat while giving instructors a transparent, easy to grade window into each learner’s understanding of diffusion models and optimization fundamentals.
