# CAPUT dataset

![](image.jpg)

Dataset for the paper Analysis of the influence of imaging-related uncertainties on cerebral aneurysm deformation quantification using a no-deformation physical flow phantom

```
Schetelig, D., Sedlacik, J., Fiehler, J., Frölich, A., Knopp, T., Sothmann, T., … Werner, R. (2018). Analysis of the influence of imaging-related uncertainties on cerebral aneurysm deformation quantification using a no-deformation physical flow phantom. Scientific Reports, 8, 11004. http://doi.org/10.1038/s41598-018-29282-0
```

## Phantom structures

```
├── Phantom
|     ├── ground_plate.stl
|     ├── inlet.stl
|     ├── Deformative_Structures
|     |    ├── 3 mm
|     |    |     ├── fusiformAneurysm.stp
|     |    |     ├── saccularAneurysm.stp
|     |    |     └── straightTube.stp
|     |    └── 4 mm
|     |          ├── fusiformAneurysm.stp
|     |          ├── saccularAneurysm.stp
|     |          └── straightTube.stp
```

## FPCT DATA

Due to the large amount of data, the data was uploaded to an external server

[Link for the FPCT Data]()

```
├── data_description.md
|
├── 4mm_fusiformAneurysm
|   ├── Data
|   └── Edges
├── 4mm_saccularAneurysm
|   ├── Data
|   └── Edges
├── 4mm_straightTube
|   ├── Data
|   └── Edges
...
```


## VIDEO DATA

Due to the large amount of data, the data was uploaded to an external server

[Link for the video data]()
```
├── data_description.md
|
├── MVI_6610
|   ├── Data
|   └── edgepoints.txt
├── MVI_6611
|   ├── Data
|   └── edgepoints.txt
├── MVI_6612
|   ├── Data
|   └── edgepoints.txt
...
```

## Registration approach

Our chosen registration approach and parameters are detailed under [ants_registration_call.md](ants_registration_call.md).
