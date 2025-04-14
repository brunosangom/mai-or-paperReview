In the presentation we should not only describe the study performed in the paper.

- ~10% of the score will be putting in context about the paper.
- ~90% of the score will be the critical analysis of the study:
    - Why did it succeed in some things?
    - Why did it fail in others?
    - What are the implications of it?

# MaGIC: Multi-modality Guided Image Completion

[MaGIC: Multi-modality Guided Image Completion](http://yeates.github.io/MaGIC-Page/)

## Abstract

- Vanilla image completion approaches:
    - Sensitivity to large missing regions → Attributed to the limited availability of reference information for plausible generation
- Existing methods incorporate the extra cue as a guidance for image completion
    - Often restricted to employing a single modality → Lacks scalability in leveraging multi-modality for more plausible completion
- Multi-modal Guided Image Completion (MaGIC):
    - Supports a wide range of single modality as the guidance
        1. Text
        2. Canny edge
        3. Sketch
        4. Segmentation
        5. Depth
        6. Pose
    - Adapts to arbitrarily customized combination of these modalities (i.e., arbitrary multi-modality) for image completion
- Components of MaGIC:
    - A modality-specific conditional U-Net (MCU-Net)
        - Injects single-modal signal into a U-Net denoiser for single-modal guided image completion
    - A consistent modality blending (CMB) method
        - Leverages modality signals encoded in multiple learned MCU-Nets through gradient guidance in latent space
        - CMB is training-free → Avoids the cumbersome joint re-training of different modalities
            - It is the secret of MaGIC to achieve exceptional flexibility in accommodating new modalities for completion
- Experiments show the superiority of MaGIC over SOTA methods and its generalization to various completion tasks