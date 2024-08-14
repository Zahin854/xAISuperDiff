# Diffusion Models for Conditional Generation of Hypothetical New Families of Superconductors

## Authors: Samuel Yuan and S.V. Dordevic

## [arXiv](https://arxiv.org/abs/2402.00198), [Website](https://www.nature.com/articles/s41598-024-61040-3)

[![DOI](https://zenodo.org/badge/DOI/10.5281/zenodo.10699906.svg)](https://doi.org/10.5281/zenodo.10699906)

This is the implementation of SuperDiff, a state-of-the-art method for computationally generating new hypothetical superconductors. SuperDiff is a new method for generating hypothetical superconductors using Diffusion Models and is the first computational superconductor generation method to generate hypothetical new families of superconductors and also the first to have support for conditioning on reference compounds. This repository contains the code, instructions, and model weights necessary to train or directly run a version of SuperDiff. SuperDiff was created by Samuel Yuan and Sasa Dordevic, you may reach us at [sdkyuan@gmail.com](mailto:sdkyuan@gmail.com) and [dsasa@uakron.edu](mailto:dsasa@uakron.edu).

<p align="center">
  <img src="https://github.com/sdkyuanpanda/SuperDiff/assets/49769610/fdf28dd9-4fdc-406b-bd3e-d4d67932ddc8" width="75%">
</p>

For ease of replication, pre-trained UNet(s) used for SuperDiff are available in `SuperDiff/checkpoints`, and `outputs` contain example raw output data from one experiment with conditional SuperDiff and the four versions of unconditional SuperDiff. Additional output data that support the results of the study are available upon reasonable request to the corresponding author at [sdkyuan@gmail.com](mailto:sdkyuan@gmail.com). 

The folder `SuperDiff` contains notebooks for some of the experiments we conducted. There, `diffusion1d-v3-[VERSION]-SAMPLE.ipynb` are the unconditional SuperDiff versions (name corresponds to class—cuprates, pnictides, etc.) and `diffusion1d_v4_ilvr_YBa1.4Sr0.6Cu3O6Se0.51.ipynb` is conditional SuperDiff trained on cuprates conditioned on YBa1.4Sr0.6Cu3O6Se0.51. Code for the other versions of conditional SuperDiff conditioned on various other compounds (including all conditional SuperDiff results presented in the table of generated new families) is available upon reasonable request to the corresponding author at [sdkyuan@gmail.com](mailto:sdkyuan@gmail.com).

<p align="center">
  <img src="https://github.com/sdkyuanpanda/SuperDiff/assets/49769610/66eefc6a-ca3a-41a4-a557-93fc49b9b08f" width="75%">
</p>

If you find this work useful, please cite it as

```
@ARTICLE{yuan2024superdiff,
  title    = "Diffusion models for conditional generation of hypothetical new
              families of superconductors",
  author   = "Yuan, Samuel and Dordevic, S V",
  abstract = "Effective computational search holds great potential for aiding
              the discovery of high-temperature superconductors (HTSs),
              especially given the lack of systematic methods for their
              discovery. Recent progress has been made in this area with
              machine learning, especially with deep generative models, which
              have been able to outperform traditional manual searches at
              predicting new superconductors within existing superconductor
              families but have yet to be able to generate completely new
              families of superconductors. We address this limitation by
              implementing conditioning---a method to control the generation
              process---for our generative model and develop SuperDiff, a
              denoising diffusion probabilistic model with iterative latent
              variable refinement conditioning for HTS discovery---the first
              deep generative model for superconductor discovery with
              conditioning on reference compounds. With SuperDiff, by being
              able to control the generation process, we were able to
              computationally generate completely new families of hypothetical
              superconductors for the very first time. Given that SuperDiff
              also has relatively fast training and inference times, it has the
              potential to be a very powerful tool for accelerating the
              discovery of new superconductors and enhancing our understanding
              of them.",
  journal  = "Scientific Reports",
  volume   =  14,
  number   =  1,
  pages    = "10275",
  month    =  may,
  year     =  2024
}
```
