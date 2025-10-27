---
mediawiki: EpiGraph
title: EpiGraph
artifact: EpiGraph
categories: [Uncategorized]
---

> **Note:** EpiGraph is designed for biological research. For detailed usage, see the manuscript: [**EpiGraph: an open-source platform to quantify epithelial organization**](https://www.biorxiv.org/content/10.1101/217521v2) and the [official lab website](https://lmescudero.blogspot.com/).

## What is EpiGraph?

[EpiGraph](/plugins/epigraph) is a Fiji plugin that measures the organization of epithelial tissues using computational geometry and graph theory.

- Cells are treated as a network: edges represent contacts.  
- Networks are split into **graphlets** (small subgraphs).  
- Comparing graphlet distributions to references gives **Graphlet Degree Distribution Distances (GDDs)**, which measure tissue organization.

**Reference patterns:**

1. **Hexagonal lattice** → Epi-Hexagons  
2. **Random Voronoi Diagram** → Epi-Random  
3. **Voronoi Diagram 5** → Epi-Voronoi5  

EpiGraph includes visualization tools, a user-friendly GUI, and Excel export. It is open-source under **GPLv3**: [GitHub](https://github.com/ComplexOrganizationOfLivingMatter/Epigraph/blob/-/LICENSE).

---

## How it works

### 5-step pipeline:

1. **Upload image & identify cells** – Upload your mosaic and detect cells.  
2. **Set neighbor distance** – Choose how to define neighboring cells.  
3. **Select ROI** – Pick the region of interest or specific cells.  
4. **Calculate graphlets** – Compute Epi-Hexagons, Epi-Random, Epi-Voronoi5. Analyze results and compare to reference patterns.  
5. **Visualize & classify** – Label images, generate 3D plots, and export data.  

---

### Installation and initial settings

[*1. Install EpiGraph*](https://github.com/ComplexOrganizationOfLivingMatter/Epigraph/raw/master/tutorials/installEpiGraph%20.mp4)

[*2. Uninstall EpiGraph*](https://github.com/ComplexOrganizationOfLivingMatter/Epigraph/raw/master/tutorials/Uninstalling%20EpiGraph.mp4)

[*3. Set the maximum RAM memory*](https://github.com/ComplexOrganizationOfLivingMatter/Epigraph/raw/master/tutorials/Select%20your%20maximum%20RAM%20memory.mp4)

### Calculation of GDDs

[*4. Calculate graphlets - default*](https://github.com/ComplexOrganizationOfLivingMatter/Epigraph/raw/master/tutorials/calculateGraphlets_default.mp4)

[*5. Calculate graphlets - select invalid region*](https://github.com/ComplexOrganizationOfLivingMatter/Epigraph/raw/master/tutorials/invalidRegion.mp4)

[*6. Calculate graphlets - squared shape*](https://github.com/ComplexOrganizationOfLivingMatter/Epigraph/raw/master/tutorials/graphletsSquareShape.mp4)

[*7. Calculate graphlets - 4 kind of motifs*](https://github.com/ComplexOrganizationOfLivingMatter/Epigraph/raw/master/tutorials/mo29_mo17_mo10_mo7.mp4)

[*8. Calculate graphlets - 4-connectivity*](https://github.com/ComplexOrganizationOfLivingMatter/Epigraph/raw/master/tutorials/connectivity4.mp4)

[*9. Calculate graphlets - ROI selection*](https://github.com/ComplexOrganizationOfLivingMatter/Epigraph/raw/master/tutorials/roiSelection.mp4)

[*10. Calculate graphlets - large image*](https://github.com/ComplexOrganizationOfLivingMatter/Epigraph/raw/master/tutorials/largeImage.mp4)

### Exporting and importing GDDs data

[*11. Export supplementary graphlets results*](https://github.com/ComplexOrganizationOfLivingMatter/Epigraph/raw/master/tutorials/exportingGraphlets.mp4)

[*12. Export and import GDDs - main window*](https://github.com/ComplexOrganizationOfLivingMatter/Epigraph/raw/master/tutorials/importExportExcel.mp4)

### Visualizing results

[*13. Visualizing window*](https://github.com/ComplexOrganizationOfLivingMatter/Epigraph/raw/master/tutorials/visualizingWindow.mp4)

## **Limitations**

EpiGraph only accepts single images right now. A stack of images should be adapted to single frames before uploading it to EpiGraph. Also, computers with little RAM memory (less than 16gb) will work but with a series of restrictions. For ensuring the usability, it is not recommended computing images with a high number of cells (more than 1000) due to a possible lack of memory. In the same way, we suggest skeletonizing the edges of the images and using a small radius (lower than 3) to calculate the cell's neighbourhood. Likewise, we warn if the input image is large (either 3000px of height or 3000px of width) in the case you have limited resources. Choosing an elevated radius value could slow down the work queue, increasing the use of RAM memory. On the other hand, computers with greater RAM memory will work with more complex and larger images and a wide range of radius.

If any of these requirements are not satisfied, the program alerts the user allowing him/her to change the image provided. Importantly, the images and the ROIs require a minimum number of cells in order to get coherent graphlets.

Regarding the 3D visualization tool, it allows the user to see the position of the samples from different angles. However, the resolution of the exported file is only 72 pixels per inch (dpi). This could be too low for publications and therefore EpiGraph provides an excel table with all the information needed to represent it with other programs. In addition, you can download any of the CVTn references (29-motifs, 17-motifs, ...) from the 'Visualizing window'.
