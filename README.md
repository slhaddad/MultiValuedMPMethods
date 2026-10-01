# MultiValuedMPMethods

This page gathers the programs that compute the **multi-valued morphological profile** of multiband images with different vector ordering algorithms. Each method has its own repository:

| Vector ordering method | Repository |
|---|---|
| AHP | [Multi-valued_MP_AHP_Method](https://github.com/slhaddad/Multi-valued_MP_AHP_Method) |
| PROMETHEE (usual preference function) | [Multi-valued_MP_PROMETHEE_Usual_Method](https://github.com/slhaddad/Multi-valued_MP_PROMETHEE_Usual_Method) |
| PROMETHEE (U-shape preference function) | [Multi-valued_MP_PROMETHEE_U-Shape_Method](https://github.com/slhaddad/Multi-valued_MP_PROMETHEE_U-Shape_Method) |
| PROMETHEE (level preference function) | [Multi-valued_MP_PROMETHEE_Level_Method](https://github.com/slhaddad/Multi-valued_MP_PROMETHEE_Level_Method) |
| PROMETHEE (Gaussian preference function) | [Multi-valued_MP_PROMETHEE_Gaussian_Method](https://github.com/slhaddad/Multi-valued_MP_PROMETHEE_Gaussian_Method) |
| QUALIFLEX | [Multi-valued_MP_QUALIFLEX_Method](https://github.com/slhaddad/Multi-valued_MP_QUALIFLEX_Method) |
| TOPSIS | [Multi-valued_MP_TOPSIS_Method](https://github.com/slhaddad/Multi-valued_MP_TOPSIS_Method) |
| SID cumulative distance | [Multi-valued_MP_SID_Method](https://github.com/slhaddad/Multi-valued_MP_SID_Method) |
| SAD cumulative distance | [Multi-valued_MP_SAD_Method](https://github.com/slhaddad/Multi-valued_MP_SAD_Method) |
| Conventional lexicographic order | [Multi-valued_MP_Lexicographic_Method](https://github.com/slhaddad/Multi-valued_MP_Lexicographic_Method) |
| Numeral system (base X) | [Multi-valued_MP_Numeral_System_Method](https://github.com/slhaddad/Multi-valued_MP_Numeral_System_Method) |
| Outranking relation | [Multi-valued_MP_Outranking_Method](https://github.com/slhaddad/Multi-valued_MP_Outranking_Method) |

All programs are written in C# (WPF, .NET 10) and share the same interface, parameters and outputs (TIFF images and ENVI multiband files). See the README of each repository for the description of the method and how to run it.

## Multivariate Mathematical Morphology through Vector Ordering

The code published in this repository implements new algorithms that extend mathematical morphology operators to multivalued images, particularly multispectral satellite images. These approaches also apply to RGB color images.

This extension relies on vector-ordering strategies applied to the pixel-vectors within the neighborhood defined by a structuring element (SE). For each neighborhood, the ordering uniquely identifies the infimum and supremum pixel-vectors required by the fundamental erosion and dilation operations.

The proposed strategies are based on:

- The comparative structure of multi-criteria decision analysis methods: AHP, PROMETHEE (usual, U-shape, level and Gaussian preference functions), QUALIFLEX and TOPSIS (p = 1 and p = 2);
- Numeral-system-based methods;
- Outranking relations between pixel-vectors;
- Cumulative distances: SID (Spectral Information Divergence) and SAD (Spectral Angle Distance);
- The conventional lexicographic order.

Each program computes multivariate erosion, dilation, opening, closing, opening by reconstruction and closing by reconstruction, using a disk-shaped structuring element of increasing size. It also exports the extended morphological profile in ENVI format.

The methods are described in detail in the following works:

- Samir, L. H., Akila, K., & Aude Nuscia, T. (2025). New Vector Ordering Algorithms for Multivalued Mathematical Morphology Computing Based on Multicriteria Decision Making Systems: L'haddad et al. *Computational and Applied Mathematics*, 44(6), 320.
- L'haddad, S., Kemmouche, A., & Taïbi, A. N. (2024). Computing Multivalued Mathematical Morphology on Multiband Images Using Algorithms for Multicriteria Analysis. *Image Analysis and Stereology*, 43(1), 23-40.
- L'haddad, S., & Kemmouche, A. (2021, January). New Approach for Multi-valued Mathematical Morphology Computation. In *International Conference on Artificial Intelligence and its Applications* (pp. 514-523). Cham: Springer International Publishing.
- L'haddad, S., & Kemmouche, A. (2020, December). Vector Ordering Algorithms for Morphological Multi-Valued Operators Using Improved F-score Technique and Numeral Systems. In *2020 4th International Symposium on Informatics and its Applications (ISIA)* (pp. 1-6). IEEE.
- Plaza, A., Martínez, P., Plaza, J., & Pérez, R. (2005). Dimensionality reduction and classification of hyperspectral image data using sequences of extended morphological transformations. *IEEE Transactions on Geoscience and Remote Sensing*, 43(3), 466-479.

A more detailed description of these methods will be provided in my forthcoming PhD thesis (in French), to be published online and on my ResearchGate profile (Samir L'Haddad, USTHB, Algiers, Algeria).
