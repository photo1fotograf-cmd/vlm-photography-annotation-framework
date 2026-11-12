# From Professional Photography Workflow to AI Training Data

**Author:** [Dejan Nikolić](https://photo-fotograf.com/) | Foto D&D Kruševac  
**Paper & Methodology (Zenodo):** [![DOI](https://zenodo.org/badge/DOI/10.5281/zenodo.24161365.svg)](https://doi.org/10.5281/zenodo.24161365)  
**Dataset (Kaggle):** [Structured AI Image Annotation Framework](https://www.kaggle.com/datasets/fotofotograf/structured-ai-image-annotation-framework)

## Overview
This repository contains the pilot data and generation scripts for a novel image annotation framework designed to translate professional commercial photography workflows into structured, machine-readable training data for Vision-Language Models (VLMs).

Standard AI datasets often rely on generic, web-scraped captions that lack technical depth. To bridge this semantic gap, this project introduces a **four-layer annotation schema**:
1. **Factual description:** Objectively visible elements.
2. **Technical analysis:** Exposure, focal length, depth of field, and optical artifacts.
3. **Contextual purpose:** Intended use case and stylistic goal.
4. **Usage decision:** Pass/fail metrics and required corrections.

### Illumination Metadata
A key feature of this framework is treating illumination quality as a primary annotation variable. The metadata block includes spectral quality metrics of the light source (CRI/Ra, R9, TLCI, CCT) to explicitly document residual hue shifts, preventing them from being silently absorbed into AI training weights.

## Repository Contents
* `pilot_annotations.jsonl` - The structured annotations for the pilot dataset.
* `generate_annotations.py` - Python script used to compile the JSONL file and calculate SHA256 hashes for data integrity.

## License
This project and dataset are licensed under the **Creative Commons Attribution 4.0 International (CC BY 4.0)**. You are free to share and adapt the material for any purpose, even commercially, as long as appropriate credit is given to the author.
