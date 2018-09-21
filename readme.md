# CAPUT dataset

Dataset for the paper Analysis of the influence of imaging-related uncertainties on cerebral aneurysm deformation quantification using a no-deformation physical flow phantom.

Due to the large amount of data, the data was uploaded to an external server:

[Download link for CAPUT image dataset]()

![](image.jpg)

```
Schetelig, D., Sedlacik, J., Fiehler, J., Frölich, A., Knopp, T., Sothmann, T., Werner, R. (2018).
Analysis of the influence of imaging-related uncertainties on cerebral aneurysm deformation quantification using a no-deformation physical flow phantom.
Scientific Reports, 8, 11004.
http://doi.org/10.1038/s41598-018-29282-0
```

## Folder / file structures

### Phantom structures

The phantom structures are stored in this repository.
The file structure is detailed below.

```
├── Phantom
      ├── ground_plate.stl
      ├── inlet.stl
      └── Deformative_Structures
            ├── 3 mm
            |     ├── fusiformAneurysm.stl
            |     ├── saccularAneurysm.stl
            |     └── straightTube.stl
            └── 4 mm
                  ├── fusiformAneurysm.stl
                  ├── saccularAneurysm.stl
                  └── straightTube.stl
```

### FPCT data file structure

All original image data and the calculated edge information are saved as NIfTI (.nii) files.

```
├── data_description.md
|
├── 4mm_fusiformAneurysm
|   ├── Data
|   |     ├── FLUSSPHANTOM_V3_t000.nii
|   |     ├── FLUSSPHANTOM_V3_t001.nii
|   |     ├── FLUSSPHANTOM_V3_t002.nii
|   |     ├── ...
|   └── Edges
|   |     └── edges.nii
├── 4mm_saccularAneurysm
|   ├── Data
|   |     ├── FLUSSPHANTOM_V3_t000.nii
|   |     ├── FLUSSPHANTOM_V3_t001.nii
|   |     ├── FLUSSPHANTOM_V3_t002.nii
|   |     ├── ...
|   └── Edges
|   |     └── edges.nii
├── 4mm_straightTube
|   ├── Data
|   |     ├── FLUSSPHANTOM_V3_t000.nii
|   |     ├── FLUSSPHANTOM_V3_t001.nii
|   |     ├── FLUSSPHANTOM_V3_t002.nii
|   |     ├── ...
|   └── Edges
|   |     └── edges.nii
...
```


### Video data file structure

```
├── 4mm_fusiformAneurysm
├── 4mm_saccularAneurysm
├── 4mm_straightTube
├── 3mm_fusiformAneurysm
├── 3mm_saccularAneurysm
└── 3mm_straightTube
...
```

### Registration approach

Our chosen registration approach and parameters are detailed under [ants_registration_call.md](ants_registration_call.md).
