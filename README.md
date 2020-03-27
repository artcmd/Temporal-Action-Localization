# Temporal Action Localization

updated on 03/26/2020

## Contents

* [Fully-supervised Action Localization](#fully-supervised-action-localization)
    * [Two-stage Localization](#two-stage-localization)
        * [Region-based Detector](#region-based-detector)
        * [Boundary-based Detector](#boundary-based-detector)
    * [One-stage Localization](#one-stage-localization)
* [Weakly-supervised Action Localization](#weakly-supervised-action-localization)
* [Results on THUMOS14](./THUMOS14.md)


## Fully-supervised Action Localization

### Two-stage Localization

#### Region-based Detector

|    | conference |     model     |                                                   paper                                                   |                          code                         |
|:--:|:----------:|:-------------:|:---------------------------------------------------------------------------------------------------------:|:-----------------------------------------------------:|
|  1 |   CVPR16   |      PSDF     | Temporal Action Localization with Pyramid of Score Distribution Features                                  |                                                       |
|  2 |   CVPR16   |     S-CNN     | Temporal Action Localization in Untrimmed Videos via Multi-stage CNNs                                     |                                                       |
|  3 |   CVPR17   |      SST      | SST: Single-Stream Temporal Action Proposals                                                              |                                                       |
|  4 |   CVPR17   |      CDC      | CDC: Convolutional-De-Convolutional Networks for Precise Temporal Action Localization in Untrimmed Videos |                                                       |
|  5 |   ICCV17   |     R-C3D     | R-C3D: Region Convolutional 3D Network for Temporal Activity Detection                                    | [Caffe](https://github.com/VisionLearningGroup/R-C3D) |
|  6 |   ICCV17   |      TURN     | TURN TAP: Temporal Unit Regression Network for Temporal Action Proposals                                  |                                                       |
|  7 |   BMVC17   |      CBR      | Cascaded Boundary Regression for Temporal Action Detection                                                |                                                       |
|  8 |   AAAI18   |      TPC      | Exploring Temporal Preservation Networks for Precise Temporal Action                                      |                                                       |
|  9 |   CVPR18   |    TAL-Net    | Rethinking the Faster R-CNN Architecture for Temporal Action Localization                                 |                                                       |
| 10 |   ECCV18   | Action Search | Action Search: Spotting Actions in Videos and Its Application to Temporal Action Localization             |                                                       |
| 11 |   ICCV19   |     P-GCN     | Graph Convolutional Networks for Temporal Action Localization                                             |     [PyTorch](https://github.com/Alvin-Zeng/PGCN)     |
| 12 |   ICCV19   |     C-TCN     | Deep Concept-wise Temporal Convolutional Networks for Action Localization                                 |                                                       |


#### Boundary-based Detector

|   | conference |    model    |                                                 paper                                                 |                                     code                                     |
|:-:|:----------:|:-----------:|:-----------------------------------------------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| 1 |   ICCV17   |   SSN+TAG   | Temporal Action Detection with Structured Segment Networks                                            |                                                                              |
| 2 |   ECCV18   |     BSN     | BSN: Boundary Sensitive Network for Temporal Action Proposal Generation                               | [PyTorch](https://github.com/wzmsltw/BSN-boundary-sensitive-network.pytorch) |
| 3 |   AAAI19   |     DBS     | Video Imprint Segmentation for Temporal Action Detection in Untrimmed Videos                          |                                                                              |
| 4 |   CVPR19   |     MGG     | Multi-Granularity Generator for Temporal Action Proposal                                              |                                                                              |
| 5 |   ICCV19   |     BMN     | BMN: Boundary-Matching Network for Temporal Action Proposal Generation                                | [PyTorch](https://github.com/JJBOY/BMN-Boundary-Matching-Network)            |
| 6 |   AAAI20   |     DBG     | Fast Learning of Temporal Action Proposal via Dense Boundary Generator                                | [TensorFlow](https://github.com/TencentYoutuResearch/ActionDetection-DBG)    |
| 7 |    TOMM    |     RAM     | Relation Attention for Temporal Action Localization                                                   |                                                                              |
| 8 |            |   TSA-Net   | Scale Matters: Temporal Scale Aggregation Network for Precise Action Localization in Untrimmed Videos |                                                                              |
| 9 |            |    IC+EC    | Constraining Temporal Relationship for Action Localization                                            |                                                                              |


### One-stage Localization

|   | conference |      model     |                                        paper                                        |                      code                      |
|:-:|:----------:|:--------------:|:-----------------------------------------------------------------------------------:|:----------------------------------------------:|
| 1 |   CVPR16   | Richard et al. | Temporal Action Detection Using a Statistical Language Model                        |                                                |
| 2 |   CVPR16   |  Yeung et al.  | End-To-End Learning of Action Detection From Frame Glimpses in Videos               |                                                |
| 3 |   CVPR17   |       SMS      | Temporal Action Localization by Structured Maximal Sums                             |                                                |
| 4 |    MM17    |      SSAD      | Single Shot Temporal Action Detection                                               |                                                |
| 5 |   BMVC17   |     SS-TAD     | End-to-End, Single-Stream Temporal Action Detection in Untrimmed Videos             | [PyTorch](https://github.com/shyamal-b/ss-tad) |
| 6 |   CVPR19   |      GTAN      | Gaussian Temporal Awareness Networks for Action Localization                        |                                                |
| 7 |   ICME19   |  Decouple-SSAD | Decoupling Localization and Classification in Single Shot Temporal Action Detection |                                                |
| 8 |            |      G-TAD     | G-TAD: Sub-Graph Localization for Temporal Action Detection                         |                                                |



## Weakly-supervised Action Localization

|    | conference |       model       |                                                  paper                                                 |                                              code                                             |
|:--:|:----------:|:-----------------:|:------------------------------------------------------------------------------------------------------:|:---------------------------------------------------------------------------------------------:|
|  1 |   CVPR17   |    UntrimmedNet   | UntrimmedNets for Weakly Supervised Action Recognition and Detection                                   |                                                                                               |
|  2 |   CVPR17   |   Richard et al.  | Weakly Supervised Action Learning With RNN Based Fine-To-Coarse Modeling                               |                                                                                               |
|  3 |   ICCV17   |   Hide-and-Seek   | Hide-and-Seek: Forcing a Network to be Meticulous for Weakly-supervised Object and Action Localization |                                                                                               |
|  4 |   CVPR18   |        STPN       | Weakly Supervised Action Localization by Sparse Temporal Pooling Network                               |                                                                                               |
|  5 |    MM18    |    Zhong et al.   | Step-by-step Erasion, One-by-one Collection: A Weakly Supervised Temporal Action Detector              |                                                                                               |
|  6 |   ECCV18   |       W-TALC      | W-TALC: Weakly-supervised Temporal Activity Localization and Classification                            |                                                                                               |
|  7 |   ECCV18   |      AutoLoc      | AutoLoc: Weakly-supervised Temporal Action Localization                                                |                                                                                               |
|  8 |   AAAI19   |        STAR       | Segregated Temporal Assembly Recurrent Networks for Weakly Supervised Multiple Action Detection        |                                                                                               |
|  9 |   ICLR19   |        MAAN       | Marginalized Average Attentional Network for Weakly-Supervised Learning                                |                                                                                               |
| 10 |   CVPR19   |        CMCS       | Completeness Modeling and Context Separation for Weakly Supervised Temporal Action Localization        | [PyTorch](https://github.com/Finspire13/CMCS-Temporal-Action-Localization)                    |
| 11 |   CVPR19   | Moltisanti et al. | Action Recognition from Single Timestamp Supervision in Untrimmed Videos                               | [PyTorch](https://bitbucket.org/dmoltisanti/action_recognition_single_timestamps/src/master/) |
| 12 |   ICCV19   |   Nguyen et al.   | Weakly-supervised Action Localization with Background Modeling                                         |                                                                                               |
| 13 |   ICCV19   |      CleanNet     | Weakly Supervised Temporal Action Localization Through Contrast Based Evaluation Networks              |                                                                                               |
| 14 |   ICCV19   |       3C-Net      | 3C-Net: Category Count and Center Loss for Weakly-Supervised Action Localization                       |                                                                                               |
| 15 |   AAAI20   |       BasNet      | Background Suppression Network for Weakly-supervised Temporal Action Localization                      | [PyTorch](https://github.com/Pilhyeon/BaSNet-pytorch)                                         |
| 16 |            |       SF-Net      | SF-Net: Single-Frame Supervision for Temporal Action Localization                                      |                                                                                               |



## Results on THUMOS14

[click this link to load full comparison](./THUMOS14.md)
