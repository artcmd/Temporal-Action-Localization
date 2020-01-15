# Temporal Action Localization on THUMOS14

updated on 01/15/2020

## Contents

* [Fully-supervised Action Localization](#fully-supervised-action-localization)
    * [Two-stage Localization](#two-stage-localization)
    * [One-stage Localization](#one-stage-localization)
* [Weakly-supervised Action Localization](#weakly-supervised-action-localization)



## Fully-supervised Action Localization

### Two-stage Localization

|    |        |     model     | approach |     proposal    |  feature |  classifier  |  0.1 |  0.2 |  0.3 |  0.4 |  0.5 |  0.6 |  0.7 |
|:--:|:------:|:-------------:|:--------:|:---------------:|:--------:|:------------:|:----:|:----:|:----:|:----:|:----:|:----:|:----:|
|  1 | CVPR16 |      PSDF     |  region  |                 | Flow+iDT |      RNN     | 51.4 | 42.6 | 33.6 | 26.1 | 18.8 |      |      |
|  2 | CVPR16 |     S-CNN     |  region  |                 |    C3D   |              | 47.7 | 43.5 | 36.3 | 28.7 | 19.0 |      |      |
|  3 | ICCV17 |     R-C3D     |  region  |                 |    C3D   |              | 54.5 | 51.5 | 44.8 | 35.6 | 28.9 |      |      |
|  4 | ICCV17 |      TURN     |  region  |       TURN      |   Flow   |     S-CNN    | 54.0 | 50.9 | 44.1 | 34.9 | 25.6 |      |      |
|  5 | BMVC17 |      CBR      |  region  |                 |    C3D   |              | 48.2 | 44.3 | 37.7 | 30.1 | 22.7 | 13.8 |  7.9 |
|  5 | BMVC17 |      CBR      |  region  |                 |  2Stream |              | 60.1 | 56.7 | 50.1 | 41.3 |  31  | 19.1 |  9.9 |
|  7 | CVPR17 |      CDC      |  region  |                 |    C3D   |     S-CNN    |      |      | 40.1 | 29.4 | 23.3 | 13.1 |  7.9 |
|  8 | AAAI18 |      TPC      |  region  |                 |    C3D   |     S-CNN    |      |      | 41.9 | 32.5 | 25.3 | 14.7 |   9  |
|  8 | AAAI18 |      TPC      |  region  |       NMS       |    C3D   |              |      |      | 44.1 | 37.1 | 28.2 | 20.6 | 12.7 |
|  9 | CVPR18 |    TAL-Net    |  region  |                 |    I3D   |              | 59.8 | 57.1 | 53.2 | 48.5 | 42.8 | 33.8 | 20.8 |
| 10 | ECCV18 | Action Search |  region  | Action Spotting |          |              |      |      | 51.8 | 42.4 | 30.8 | 20.2 | 11.1 |
| 11 | ICCV19 |     P-GCN     |  region  |       BSN       |    I3D   |              | 69.5 | 67.8 | 63.6 | 57.8 | 49.1 |      |      |
| 12 | ICCV19 |     C-TCN     |  region  |                 |    I3D   |              | 72.2 | 71.4 | 68.0 | 62.3 | 52.1 |      |      |
|  1 | ICCV17 |      SSN      | boundary |       TAG       |  2Stream |              | 60.3 | 56.2 | 50.6 | 40.8 | 29.1 |      |      |
|  2 | ECCV18 |      BSN      | boundary |                 |          |     S-CNN    |      |      | 43.1 | 36.6 | 29.4 | 22.4 | 15.0 |
|  2 | ECCV18 |      BSN      | boundary |                 |          | UntrimmedNet |      |      | 53.5 | 45.0 | 36.9 | 28.4 | 20.0 |
|  3 | AAAI19 |      DBS      | boundary |                 |          |              | 56.7 | 54.7 | 50.6 | 43.1 | 34.3 | 24.4 | 14.7 |
|  4 | CVPR19 |      MGG      | boundary |                 |          |     S-CNN    |      |      | 44.9 | 37.8 | 29.9 | 23.6 | 15.8 |
|  4 | CVPR19 |      MGG      | boundary |                 |          | UntrimmedNet |      |      | 53.9 | 46.8 | 37.4 | 29.5 | 21.3 |
|  5 | ICCV19 |      BMN      | boundary |                 |          |     S-CNN    |      |      | 45.7 | 40.2 | 32.2 | 24.5 | 17.0 |
|  5 | ICCV19 |      BMN      | boundary |                 |          | UntrimmedNet |      |      | 56.0 | 47.4 | 38.8 | 29.7 | 20.5 |
|  6 | AAAI20 |      DBG      | boundary |                 |          |     S-CNN    |      |      | 45.9 | 40.4 | 32.9 | 25.3 | 18.4 |
|  6 | AAAI20 |      DBG      | boundary |                 |          | UntrimmedNet |      |      | 57.8 | 49.4 | 39.8 | 30.2 | 21.7 |



### One-stage Localization

|   |        |     model    |  approach |   feature   |  0.1 |  0.2 |  0.3 |  0.4 |  0.5 |
|:-:|:------:|:------------:|:---------:|:-----------:|:----:|:----:|:----:|:----:|:----:|
| 2 | CVPR16 | Yeung et al. | one-stage |    VGG16    | 48.9 | 44.0 | 36.0 | 26.4 | 17.1 |
| 3 | CVPR17 |      SMS     | one-stage |   2Stream   | 51.0 | 45.2 | 36.5 | 27.8 | 17.8 |
| 4 |  MM17  |     SSAD     | one-stage | 2Stream+C3D | 50.1 | 47.8 | 43.0 | 35.0 | 24.6 |
| 5 | CVPR19 |     GTAN     | one-stage |     C3D     | 67.2 | 61.1 | 56.9 | 46.5 | 37.9 |
| 5 | CVPR19 |     GTAN     | one-stage |     P3D     | 69.1 | 63.7 | 57.8 | 47.2 | 38.8 |



## Weakly-supervised Action Localization

