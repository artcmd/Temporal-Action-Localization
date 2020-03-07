# Temporal Action Localization on THUMOS14

updated on 03/07/2020

## Contents

* [Fully-supervised Action Localization](#fully-supervised-action-localization)
    * [Proposal Generator](#proposal-generator)
    * [Two-stage Localization](#two-stage-localization)
    * [One-stage Localization](#one-stage-localization)
* [Weakly-supervised Action Localization](#weakly-supervised-action-localization)



## Fully-supervised Action Localization

### Proposal Generator

**metric: AR@AN** (Average Recall with different Average Numbers of proposals)

|   |        |   model   | approach | feature | surpression |  @50  |  @100 |  @200 |  @500 | @1000 |
|:-:|:------:|:---------:|:--------:|:-------:|:-----------:|:-----:|:-----:|:-----:|:-----:|:-----:|
| 2 | CVPR16 | SCNN-prop |  region  |   C3D   |             | 17.22 | 26.17 | 37.01 | 51.57 | 58.20 |
| 3 | CVPR17 |    SST    |  region  |   C3D   |             | 19.90 | 28.36 | 37.90 | 51.58 | 60.27 |
| 6 | ICCV17 |    TURN   |  region  |   C3D   |             | 19.63 | 27.96 | 38.34 | 53.52 | 60.75 |
| 2 | ECCV18 |    BSN    | boundary |   C3D   |     NMS     | 27.19 | 35.38 | 43.61 | 53.77 | 59.50 |
| 2 | ECCV18 |    BSN    | boundary |   C3D   |   Soft-NMS  | 29.58 | 37.38 | 45.55 | 54.67 | 59.48 |
| 4 | CVPR19 |    MGG    | boundary |   C3D   |             | 29.11 | 36.31 | 44.32 | 54.95 | 60.98 |
| 5 | ICCV19 |    BMN    | boundary |   C3D   |     NMS     | 29.04 | 37.72 | 46.79 | 56.07 | 60.96 |
| 5 | ICCV19 |    BMN    | boundary |   C3D   |   Soft-NMS  | 32.73 | 40.68 | 47.86 | 56.42 | 60.44 |
| 6 | AAAI20 |    DBG    | boundary |   C3D   |     NMS     | 32.55 | 41.07 | 48.83 | 57.58 | 59.55 |
| 6 | AAAI20 |    DBG    | boundary |   C3D   |   Soft-NMS  | 30.55 | 38.82 | 46.59 | 56.42 | 62.17 |
| 8 |        |  TSA-Net  | boundary |   C3D   |     NMS     | 31.88 | 40.19 | 46.28 |       |       |
| 8 |        |  TSA-Net  | boundary |   C3D   |   Soft-NMS  | 34.00 | 41.11 | 47.51 |       |       |
| 1 | ICCV17 |    TAG    | boundary | 2Stream |             | 18.55 | 29.00 | 39.61 |       |       |
| 2 | ECCV18 |    BSN    | boundary | 2Stream |     NMS     | 35.41 | 43.55 | 52.23 | 61.35 | 65.10 |
| 2 | ECCV18 |    BSN    | boundary | 2Stream |   Soft-NMS  | 37.46 | 46.06 | 53.21 | 60.64 | 64.52 |
| 4 | CVPR19 |    MGG    | boundary | 2Stream |             | 39.93 | 47.75 | 54.65 | 61.36 | 64.06 |
| 5 | ICCV19 |    BMN    | boundary | 2Stream |     NMS     | 37.15 | 46.75 | 54.84 | 62.19 | 65.22 |
| 5 | ICCV19 |    BMN    | boundary | 2Stream |   Soft-NMS  | 39.36 | 47.72 | 54.70 | 62.07 | 65.49 |
| 6 | AAAI20 |    DBG    | boundary | 2Stream |     NMS     | 40.89 | 49.24 | 55.76 | 61.43 | 61.95 |
| 6 | AAAI20 |    DBG    | boundary | 2Stream |   Soft-NMS  | 37.32 | 46.67 | 54.50 | 62.21 | 66.40 |
| 8 |        |  TSA-Net  | boundary | 2Stream |     NMS     | 41.40 | 48.70 | 53.57 |       |       |
| 8 |        |  TSA-Net  | boundary | 2Stream |   Soft-NMS  | 42.83 | 49.61 | 54.52 |       |       |
| 9 |        |   IC+EC   | boundary | 2Stream |   Soft-NMS  | 44.23 | 50.67 | 55.74 |       |       |
| 8 |        |  TSA-Net  | boundary |   P3D   |     NMS     | 45.84 | 52.29 | 56.17 |       |       |
| 8 |        |  TSA-Net  | boundary |   P3D   |   Soft-NMS  | 46.77 | 53.15 | 57.68 |       |       |


### Two-stage Localization

**metric: tIoU**

|    |        |     model     | approach |     proposal    |  feature |  classifier  |  0.1 |  0.2 |  0.3 |  0.4 |  0.5 |  0.6 |  0.7 |
|:--:|:------:|:-------------:|:--------:|:---------------:|:--------:|:------------:|:----:|:----:|:----:|:----:|:----:|:----:|:----:|
|  1 | CVPR16 |      PSDF     |  region  |                 | Flow+iDT |      RNN     | 51.4 | 42.6 | 33.6 | 26.1 | 18.8 |      |      |
|  2 | CVPR16 |     S-CNN     |  region  |                 |    C3D   |              | 47.7 | 43.5 | 36.3 | 28.7 | 19.0 |      |      |
|  4 | CVPR17 |      CDC      |  region  |                 |    C3D   |     S-CNN    |      |      | 40.1 | 29.4 | 23.3 | 13.1 |  7.9 |
|  5 | ICCV17 |     R-C3D     |  region  |                 |    C3D   |              | 54.5 | 51.5 | 44.8 | 35.6 | 28.9 |      |      |
|  6 | ICCV17 |      TURN     |  region  |       TURN      |    C3D   |     S-CNN    | 48.8 | 45.5 | 40.3 | 31.5 | 22.5 |      |      |
|  6 | ICCV17 |      TURN     |  region  |       TURN      |   Flow   |     S-CNN    | 54.0 | 50.9 | 44.1 | 34.9 | 25.6 |      |      |
|  7 | BMVC17 |      CBR      |  region  |                 |    C3D   |              | 48.2 | 44.3 | 37.7 | 30.1 | 22.7 | 13.8 |  7.9 |
|  7 | BMVC17 |      CBR      |  region  |                 |  2Stream |              | 60.1 | 56.7 | 50.1 | 41.3 |  31  | 19.1 |  9.9 |
|  8 | AAAI18 |      TPC      |  region  |                 |    C3D   |     S-CNN    |      |      | 41.9 | 32.5 | 25.3 | 14.7 |   9  |
|  8 | AAAI18 |      TPC      |  region  |       NMS       |    C3D   |              |      |      | 44.1 | 37.1 | 28.2 | 20.6 | 12.7 |
|  9 | CVPR18 |    TAL-Net    |  region  |                 |    I3D   |              | 59.8 | 57.1 | 53.2 | 48.5 | 42.8 | 33.8 | 20.8 |
| 10 | ECCV18 | Action Search |  region  | Action Spotting |          |              |      |      | 51.8 | 42.4 | 30.8 | 20.2 | 11.1 |
| 11 | ICCV19 |     P-GCN     |  region  |       BSN       |    I3D   |              | 69.5 | 67.8 | 63.6 | 57.8 | 49.1 |      |      |
| 12 | ICCV19 |     C-TCN     |  region  |                 |    I3D   |              | 72.2 | 71.4 | 68.0 | 62.3 | 52.1 |      |      |
|  1 | ICCV17 |      SSN      | boundary |       TAG       |  2Stream |              | 60.3 | 56.2 | 50.6 | 40.8 | 29.1 |      |      |
|  2 | ECCV18 |      BSN      | boundary |                 |  2Stream |     S-CNN    |      |      | 43.1 | 36.6 | 29.4 | 22.4 | 15.0 |
|  2 | ECCV18 |      BSN      | boundary |                 |  2Stream | UntrimmedNet |      |      | 53.5 | 45.0 | 36.9 | 28.4 | 20.0 |
|  3 | AAAI19 |      DBS      | boundary |                 |          |              | 56.7 | 54.7 | 50.6 | 43.1 | 34.3 | 24.4 | 14.7 |
|  4 | CVPR19 |      MGG      | boundary |                 |  2Stream |     S-CNN    |      |      | 44.9 | 37.8 | 29.9 | 23.6 | 15.8 |
|  4 | CVPR19 |      MGG      | boundary |                 |  2Stream | UntrimmedNet |      |      | 53.9 | 46.8 | 37.4 | 29.5 | 21.3 |
|  5 | ICCV19 |      BMN      | boundary |                 |  2Stream |     S-CNN    |      |      | 45.7 | 40.2 | 32.2 | 24.5 | 17.0 |
|  5 | ICCV19 |      BMN      | boundary |                 |  2Stream | UntrimmedNet |      |      | 56.0 | 47.4 | 38.8 | 29.7 | 20.5 |
|  6 | AAAI20 |      DBG      | boundary |       TSN       |  2Stream |     S-CNN    |      |      | 45.9 | 40.4 | 32.9 | 25.3 | 18.4 |
|  6 | AAAI20 |      DBG      | boundary |       TSN       |  2Stream | UntrimmedNet |      |      | 57.8 | 49.4 | 39.8 | 30.2 | 21.7 |
|  7 |  ToMM  |      RAM      | boundary |       TAG       |  SSN+RAM |              | 65.4 | 63.1 | 58.8 | 52.7 | 43.7 |      |      |
|  8 |        |    TSA-Net    | boundary |                 |  2Stream |     S-CNN    |      |      | 43.7 | 39.2 | 33.1 | 25.2 | 17.1 |
|  8 |        |    TSA-Net    | boundary |                 |    P3D   |     S-CNN    |      |      | 48.3 | 43.7 | 36.6 | 27.8 | 19.4 |
|  8 |        |    TSA-Net    | boundary |                 |  2Stream | UntrimmedNet |      |      | 53.2 | 48.1 | 41.5 | 31.5 | 21.7 |
|  8 |        |    TSA-Net    | boundary |                 |    P3D   | UntrimmedNet |      |      | 61.2 | 55.9 | 46.9 | 36.1 | 25.2 |
|  9 |        |     IC+EC     | boundary |                 |    I3D   |              |      |      | 53.9 | 50.7 | 45.4 | 38.0 | 28.5 |


### One-stage Localization

**metric: tIoU**

|   |        |     model     |  approach |       feature      |  0.1 |  0.2 |  0.3 |  0.4 |  0.5 |  0.6 |  0.7 |
|:-:|:------:|:-------------:|:---------:|:------------------:|:----:|:----:|:----:|:----:|:----:|:----:|:----:|
| 2 | CVPR16 |  Yeung et al. | one-stage |        VGG16       | 48.9 | 44.0 | 36.0 | 26.4 | 17.1 |      |      |
| 3 | CVPR17 |      SMS      | one-stage |       2Stream      | 51.0 | 45.2 | 36.5 | 27.8 | 17.8 |      |      |
| 4 |  MM17  |      SSAD     | one-stage |     2Stream+C3D    | 50.1 | 47.8 | 43.0 | 35.0 | 24.6 |      |      |
| 5 | BMVC17 |     SS-TAD    | one-stage |                    |      |      | 45.7 |      | 29.2 |      |  9.6 |
| 6 | CVPR19 |      GTAN     | one-stage |         C3D        | 67.2 | 61.1 | 56.9 | 46.5 | 37.9 |      |      |
| 6 | CVPR19 |      GTAN     | one-stage |         P3D        | 69.1 | 63.7 | 57.8 | 47.2 | 38.8 |      |      |
| 7 | ICME19 | Decouple-SSAD | one-stage |  2Stream (UCF101)  |      |      | 49.9 | 44.4 | 35.8 | 24.3 | 13.6 |
| 7 | ICME19 | Decouple-SSAD | one-stage | 2Stream (Kinetics) |      |      | 60.2 | 54.1 | 44.2 | 32.3 | 19.1 |
| 8 |        |     G-TAD     | one-stage |       GCNeXt       |      |      | 54.5 | 47.6 | 40.2 | 30.8 | 23.4 |


## Weakly-supervised Action Localization

**metric: tIoU**

|    |        |      model     | approach |     feature     |  0.1 |  0.2 |  0.3 |  0.4 |  0.5 |  0.6 |  0.7 |
|:--:|:------:|:--------------:|:--------:|:---------------:|:----:|:----:|:----:|:----:|:----:|:----:|:----:|
|  1 | CVPR17 |  UntrimmedNet  |   weak   |     2Stream     | 44.4 | 37.7 | 28.2 | 21.1 | 13.7 |      |      |
|  2 | CVPR17 | Richard et al. |   weak   |                 |      |      |      |      |      |      |      |
|  3 | ICCV17 |  Hide-and-Seek |   weak   |     AlexNet     | 36.4 | 27.8 | 19.5 | 12.7 |  6.8 |      |      |
|  4 | CVPR18 |      STPN      |   weak   |   UntrimmedNet  | 45.3 | 38.8 | 31.1 | 23.5 | 16.2 |  9.8 |  5.1 |
|  4 | CVPR18 |      STPN      |   weak   |       I3D       | 52.0 | 44.7 | 35.5 | 25.8 | 16.9 |  9.9 |  4.3 |
|  5 |  MM18  |  Zhong et al.  |   weak   |       TSN       | 45.8 | 39.0 | 31.1 | 22.5 | 15.9 |      |      |
|  6 | ECCV18 |     W-TALC     |   weak   |   UntrimmedNet  | 49.0 | 42.8 | 32.0 | 26.0 | 18.8 |      |  6.2 |
|  6 | ECCV18 |     W-TALC     |   weak   |       I3D       | 55.2 | 49.6 | 40.1 | 31.1 | 22.8 |      |  7.6 |
|  7 | ECCV18 |     AutoLoc    |   weak   |       TSN       |      |      | 35.8 | 29.0 | 21.2 | 13.4 |  5.8 |
|  8 | AAAI19 |      STAR      |   weak   |       I3D       | 68.8 | 60.0 | 48.7 | 34.7 | 23.0 |      |      |
|  9 | ICLR19 |      MAAN      |   weak   |       I3D       | 59.8 | 50.8 | 41.1 | 30.6 | 20.3 | 12.0 |  6.9 |
| 10 | CVPR19 |      CMCS      |   weak   |   UntrimmedNet  | 53.5 | 46.8 | 37.5 | 29.1 | 19.9 | 12.3 |  6.0 |
| 10 | CVPR19 |      CMCS      |   weak   |       I3D       | 57.4 | 50.8 | 41.2 | 32.1 | 23.1 | 15.0 |  7.0 |
| 11 | ICCV19 |  Nguyen et al. |   weak   |       I3D       | 60.4 | 56.0 | 46.6 | 37.5 | 26.8 | 17.6 |  9.0 |
| 11 | ICCV19 |  Nguyen et al. |   weak   | I3D+microvideos | 64.2 | 59.5 | 49.1 | 38.4 | 27.5 | 17.3 |  8.6 |
| 12 | ICCV19 |    CleanNet    |   weak   |       TSN       |      |      | 36.3 | 30.7 | 22.9 | 13.8 |  5.3 |
| 12 | ICCV19 |    CleanNet    |   weak   |       TSN*      |      |      | 37.0 | 30.9 | 23.9 | 13.9 |  7.1 |
| 13 | ICCV19 |     3C-Net     |   weak   |       I3D       | 59.1 | 53.5 | 44.2 | 34.1 | 26.6 |      |  8.1 |
| 14 | AAAI20 |     BasNet     |   weak   |   UntrimmedNet  | 56.2 | 50.3 | 42.8 | 34.7 | 25.1 | 17.1 |  9.3 |
| 14 | AAAI20 |     BasNet     |   weak   |       I3D       | 58.2 | 52.3 | 44.6 | 36.0 | 27.0 | 18.6 | 10.4 |
