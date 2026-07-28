# Dual-Modality DESI-MSI METASPACE-to-AnnData/SpatialData Integration Pipeline

## Overview
The Stanford Center for Imaging Mass Spectrometry (SCIMS) was established within the Stanford University Mass Spectrometry (SUMS) facility in 2023 to provide comprehensive support for mass spectrometry imaging (MSI) studies. Our services include consultation on sample preparation, MSI data acquisition, data processing, and uploading processed datasets to METASPACE for visualization and annotation.
As MSI continues to evolve toward spatial multiomics, SCIMS is expanding its capabilities beyond data acquisition to include consultation on experimental design for the MSI component of multimodal studies, as well as the development of downstream multimodal data integration and analysis workflows.
In June 2026, METASPACE released the METASPACE Converter, a Python package that exports METASPACE datasets directly to AnnData and SpatialData, two widely adopted data formats in the scverse ecosystem for single-cell and spatial omics analysis. By enabling seamless integration of METASPACE datasets with other spatial omics modalities, this tool provides a foundation for multimodal data analysis.
The aim of this poster is to establish an initial METASPACE–AnnData–SpatialData workflow using datasets currently available in our laboratory. As a proof of concept, we analyzed a mouse brain tumor section acquired by DESI MSI in two complementary modalities: negative-ion lipid imaging and positive-ion metabolite imaging on the same tissue section. Both datasets were annotated in METASPACE and exported to AnnData format using the METASPACE Converter. The datasets were then co-registered, integrated into a single SpatialData object, and processed by removing off-tissue background signals and extracting the on-tissue region of interest (ROI). Leiden clustering was subsequently performed, and the resulting spatial distributions were visualized using SpatialData and Matplotlib.
A key feature of this project was the use of OpenAI Codex as an interactive programming assistant. By leveraging the official GitHub documentation for the METASPACE Converter, AnnData, and SpatialData, Codex accelerated our understanding of these tools by explaining functions, troubleshooting errors, and generating Python code tailored to our analysis needs. It also assisted in designing the co-registration workflow and extending the Napari interface with custom features for ROI selection and optical image overlay. Overall, Codex substantially lowered the barrier to adopting modern Python-based spatial omics tools, enabling researchers with limited programming experience to rapidly develop and implement advanced multimodal data analysis workflows.

## Workflow
<img width="1231" height="1553" alt="image" src="https://github.com/user-attachments/assets/8f404ed7-8c8e-47a8-9f87-1f6d0ca0ac5a" />

## Requirements
Python, METASPACE account/API key, AnnData, SpatialData, Scanpy, Napari.

## Example Pipeline
Step-by-step commands.

## Example Outputs
<img width="648" height="304" alt="Screenshot 2026-07-27 at 9 15 19 PM" src="https://github.com/user-attachments/assets/1f727b79-47e2-4aab-bf2f-ef46d1df441d" />
<img width="989" height="485" alt="Screenshot 2026-07-27 at 9 17 27 PM" src="https://github.com/user-attachments/assets/039b7969-944c-4f4d-91c9-c9b2e42632b8" />
<img width="989" height="485" alt="Screenshot 2026-07-27 at 9 17 46 PM" src="https://github.com/user-attachments/assets/7ff89a03-37b5-40ec-a693-a7ba06ad1138" />


## Notes
Manual XY registration, ROI selection, limitations.
