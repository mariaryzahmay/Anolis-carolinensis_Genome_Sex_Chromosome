# Anolis-carolinensis_Genome_Sex_Chromosome

# Cytoskeleton and Cell Morphology Analysis (BBBC018)

**Karp Chapter 9: The Cytoskeleton and Cell Motility**

**Student ID:** [202400735]  
**Dataset:** BBBC018 - Human HT29 Colon-Cancer Cells  
**Selected Phenotype:** Anaphase/Telophase  
**Image-Field ID:** [To be determined]

---

## Introduction

The cytoskeleton plays an important role in maintaining cell shape, providing structural support, and coordinating cellular activities such as cell division. In this activity, fluorescence images of HT29 human colon-cancer cells from the BBBC018 dataset were examined to observe F-actin distribution and cell morphology during mitosis.

The selected phenotype was Anaphase/Telophase, which represents the later stages of mitotic cell division. During anaphase, sister chromatids separate and move toward opposite poles of the cell, while telophase involves the formation of two new nuclei. Five cells were measured using Fiji, and their measurements were analyzed in R to compare cell area, circularity, aspect ratio, and mean actin fluorescence intensity.

---

## Dataset and Selected Images

The fluorescence images were obtained from the Broad Bioimage Benchmark Collection (BBBC018).

- **Dataset:** [BBBC018](https://bbbc.broadinstitute.org/BBBC018)
- **Download:** [BBBC018_v1_images.zip](https://data.broadinstitute.org/bbbc/BBBC018/BBBC018_v1_images.zip)
- **Phenotype:** Anaphase/Telophase
- **Image-field ID:** [To be determined]
- **Actin filename:** `[IMAGE-ID]-actin.DIB`
- **DNA filename:** `[IMAGE-ID]-DNA.DIB`

The actin channel was used to examine F-actin staining and trace cell boundaries, while the DNA channel served as a guide for identifying chromosomes and observing their arrangement during anaphase and telophase. These two fluorescence channels helped distinguish the cellular structures associated with the selected mitotic phenotype.

---

## Methods

### Fiji Analysis

- The matching actin and DNA fluorescence images were opened in Fiji using Bio-Formats.
- Cell outlines and DNA staining patterns were examined to identify cells displaying features associated with anaphase or telophase.
- Five intact cells with distinguishable boundaries were selected for measurement.
- Area, Mean gray value, Shape descriptors, and Display label were enabled under Set Measurements.
- The Freehand Selection tool was used to trace the outer boundaries of each cell, and the selections were added to ROI Manager.
- All five cells were measured, and the measurements were saved as `data/fiji_results.csv`.
- The annotated fluorescence image showing the five labeled cells was saved as `figures/measured_cells.png`.

### R Analysis

- The Fiji measurements were imported into RStudio using an R script.
- Following the provided R code, the mean cell area, circularity, aspect ratio, and actin fluorescence intensity of the five measured cells were calculated.
- Two graphs were generated using the provided R code to compare cell area versus circularity and the mean actin fluorescence intensity of the five cells.
- The numerical summary and generated figures were saved in the results and figures folders, respectively.

---

## Results

The following figures present the results of the cell morphology analysis using Fiji and RStudio. Five HT29 cells from image field [IMAGE-ID] were examined to determine their cell area, circularity, aspect ratio, and mean F-actin fluorescence intensity.

### Five Measured HT29 Cells

The fluorescence image was opened in Fiji, where five cells with distinguishable boundaries were selected and traced using the Freehand Selection tool. The matching DNA channel was used as a reference for observing chromosome arrangements and identifying the selected mitotic phenotype. Each cell outline was added to ROI Manager, and the Show All and Labels options were enabled to display the five numbered outlines. The annotated image was then saved for documentation.

[Insert link to measured_cells.png]

**Figure 1.** F-actin fluorescence image of HT29 cells from field [IMAGE-ID], showing the five selected cells outlined and numbered using Fiji.

### Cell Area versus Circularity

Using the measurements obtained from Fiji, a scatter plot was generated in RStudio to examine the relationship between cell area and circularity among the five measured cells.

[Insert link to area_vs_circularity.png]

**Figure 2.** Scatter plot showing the relationship between cell area and circularity among the five measured HT29 cells.

The cells had areas ranging from [MINIMUM AREA] to [MAXIMUM AREA] pixels², with Cell [NUMBER] having the largest area. Circularity values ranged from [MINIMUM CIRCULARITY] to [MAXIMUM CIRCULARITY], with a mean of [MEAN CIRCULARITY]. These measurements describe the differences in cell size and shape among the selected cells. The circularity values indicate whether the cells were generally rounded or had more irregular outlines.

### Mean Actin Fluorescence Intensity

A bar graph was also generated using the provided R code to compare the mean F-actin fluorescence intensity of the five measured cells.

[Insert link to actin_intensity.png]

**Figure 3.** Bar graph comparing the mean F-actin fluorescence intensity of five HT29 cells from image field [IMAGE-ID].

Cell [NUMBER] showed the highest mean F-actin fluorescence intensity at [HIGHEST VALUE] AU, while Cell [NUMBER] obtained the lowest at [LOWEST VALUE] AU. The average intensity across all five cells was [MEAN INTENSITY] AU. These results indicate variations in F-actin fluorescence intensity among the measured cells, suggesting differences in the intensity of actin staining within the selected image field.

---

### Cell Measurement Summary

The table below presents the average measurements of the five selected HT29 cells obtained through Fiji and analyzed using RStudio.

| Measurement | Mean Value |
|---|---|
| Cell area | [MEAN AREA] pixels² |
| Circularity | [MEAN CIRCULARITY] |
| Aspect ratio | [MEAN ASPECT RATIO] |
| Actin fluorescence intensity | [MEAN INTENSITY] AU |

The five measured cells had an average area of [MEAN AREA] pixels², indicating the overall size of the selected cells. The mean circularity of [MEAN CIRCULARITY] and aspect ratio of [MEAN ASPECT RATIO] describe their general morphology. Meanwhile, the average F-actin fluorescence intensity of [MEAN INTENSITY] AU represents the overall mean actin staining signal of the five cells within the selected image field.

---

## Guide Questions

***1. Which specific phenotype did you choose, and what visible features support that choice?***

Anaphase/Telophase was my chosen phenotype. In the fluorescence image, the DNA channel can show features associated with chromosome separation during anaphase or the formation of two distinct groups of DNA during telophase. These observations help distinguish cells undergoing the later stages of mitotic division.

***2. Were your five cells mostly round or elongated? Refer to your circularity and aspect-ratio results.***

The five measured cells were generally [rounded/elongated], with an average circularity of [VALUE] and an average aspect ratio of [VALUE]. These measurements indicate the overall shape and degree of elongation of the selected cells. The circularity and aspect-ratio values provide a quantitative basis for describing their morphology.

***3. What role does actin play in maintaining cell shape and in cell movement (Karp Chapter 9)?***

Actin is a major component of the cytoskeleton that provides structural support and helps maintain cell shape. During cell division, actin filaments interact with myosin to form a contractile ring that helps divide the cytoplasm during cytokinesis. Actin also contributes to cell movement through the formation of structures such as lamellipodia and filopodia, allowing cells to change their shape and move.

***4. Why can a single fixed fluorescence image NOT show how fast a cell moves?***

A single fixed fluorescence image captures the structure and organization of a cell at only one point in time. Although it can reveal cellular features and the arrangement of stained structures, it cannot show changes in cell position over time. Therefore, cell movement speed cannot be determined from a single fixed image.

---

## Conclusion

The analysis of five HT29 cells provided an opportunity to examine cell morphology and F-actin organization in a fluorescence image representing the Anaphase/Telophase phenotype. The measurements of cell area, circularity, aspect ratio, and actin fluorescence intensity demonstrated variations in the size, shape, and staining intensity of the selected cells. The activity also highlighted the importance of the cytoskeleton, particularly actin filaments, in maintaining cell structure and contributing to cytokinesis during cell division. Taken together, the activity demonstrated how fluorescence microscopy, Fiji, and R can be used to examine cellular morphology and cytoskeletal organization.

---

## References and Data Sources

Broad Bioimage Benchmark Collection. (n.d.). *BBBC018: Human HT29 colon-cancer cells (diverse phenotypes).* Broad Institute. https://bbbc.broadinstitute.org/BBBC018

Ljosa, V., Sokolnicki, K. L., & Carpenter, A. E. (2012). Annotated high-throughput microscopy image sets for validation. *Nature Methods, 9*(7), 637. https://doi.org/10.1038/nmeth.2083

### Data Credit and Image License

**Data Credit:** We used image set BBBC018v1 from the Broad Bioimage Benchmark Collection (Ljosa et al., Nature Methods, 2012).

**Image License:** Creative Commons Attribution-NonCommercial-ShareAlike 3.0 (CC BY-NC-SA 3.0).
