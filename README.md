# Temporal Action Localization

updated on 01/14/2020

## Contents

* [Fully-supervised Action Localization](#fully-supervised-action-localization)
    * [Two-stage Localization](#two-stage-localization)
        * [Region-based Detector](#region-based-detector)
        * [Boundary-based Detector](#boundary-based-detector)
    * [One-stage Localization](#one-stage-localization)
* [Weakly-supervised Action Localization](#weakly-supervised-action-localization)



## Fully-supervised Action Localization

### Two-stage Localization

#### Region-based Detector

| conference |     model     |                                                   paper                                                   |
|:----------:|:-------------:|:---------------------------------------------------------------------------------------------------------:|
|   CVPR16   |      PSDF     |                  Temporal Action Localization with Pyramid of Score Distribution Features                 |
|   CVPR16   |     S-CNN     |                   Temporal Action Localization in Untrimmed Videos via Multi-stage CNNs                   |
|   ICCV17   |     R-C3D     |                   R-C3D: Region Convolutional 3D Network for Temporal Activity Detection                  |
|   ICCV17   |      TURN     |                  TURN TAP: Temporal Unit Regression Network for Temporal Action Proposals                 |
|   BMVC17   |      CBR      |                         Cascaded Boundary Regression for Temporal Action Detection                        |
|   CVPR17   |      SST      |                                SST: Single-Stream Temporal Action Proposals                               |
|   CVPR17   |      CDC      | CDC: Convolutional-De-Convolutional Networks for Precise Temporal Action Localization in Untrimmed Videos |
|   AAAI18   |      TPC      |                    Exploring Temporal Preservation Networks for Precise Temporal Action                   |
|   CVPR18   |    TAL-Net    |                 Rethinking the Faster R-CNN Architecture for Temporal Action Localization                 |
|   ECCV18   | Action Search |       Action Search: Spotting Actions in Videos and Its Application to Temporal Action Localization       |
|   ICCV19   |     P-GCN     |                       Graph Convolutional Networks for Temporal Action Localization                       |
|   ICCV19   |     C-TCN     |                 Deep Concept-wise Temporal Convolutional Networks for Action Localization                 |


#### Boundary-based Detector

| conference |  model  |                                     paper                                    |
|:----------:|:-------:|:----------------------------------------------------------------------------:|
|   ICCV17   | SSN+TAG |          Temporal Action Detection with Structured Segment Networks          |
|   ECCV18   |   BSN   |    BSN: Boundary Sensitive Network for Temporal Action Proposal Generation   |
|   AAAI19   |   DBS   | Video Imprint Segmentation for Temporal Action Detection in Untrimmed Videos |
|   CVPR19   |   MGG   |           Multi-Granularity Generator for Temporal Action Proposal           |
|   ICCV19   |   BMN   |    BMN: Boundary-Matching Network for Temporal Action Proposal Generation    |
|   AAAI20   |   DBG   |    Fast Learning of Temporal Action Proposal via Dense Boundary Generator    |



### One-stage Localization

| conference | model |                                 paper                                 |
|:----------:|:-----:|:---------------------------------------------------------------------:|
|   CVPR16   |       | Temporal Action Detection Using a Statistical Language Model          |
|   CVPR16   |       | End-To-End Learning of Action Detection From Frame Glimpses in Videos |
|   CVPR17   |  SMS  | Temporal Action Localization by Structured Maximal Sums               |
|    MM17    |  SSAD | Single Shot Temporal Action Detection                                 |
|   CVPR19   |  GTAN | Gaussian Temporal Awareness Networks for Action Localization          |



## Weakly-supervised Action Localization

| conference |     model     |                                                  paper                                                 |
|:----------:|:-------------:|:------------------------------------------------------------------------------------------------------:|
|   CVPR17   |  UntrimmedNet | UntrimmedNets for Weakly Supervised Action Recognition and Detection                                   |
|   CVPR17   |               | Weakly Supervised Action Learning With RNN Based Fine-To-Coarse Modeling                               |
|   ICCV17   | Hide-and-Seek | Hide-and-Seek: Forcing a Network to be Meticulous for Weakly-supervised Object and Action Localization |
|   CVPR18   |      STPN     | Weakly Supervised Action Localization by Sparse Temporal Pooling Network                               |
|    MM18    |               | Step-by-step Erasion, One-by-one Collection: A Weakly Supervised Temporal Action Detector              |
|   ECCV18   |     W-TALC    | W-TALC: Weakly-supervised Temporal Activity Localization and Classification                            |
|   ECCV18   |    AutoLoc    | AutoLoc: Weakly-supervised Temporal Action Localization                                                |
|   AAAI19   |               | Segregated Temporal Assembly Recurrent Networks for Weakly Supervised Multiple Action Detection        |
|   ICLR19   |      MAAN     | Marginalized Average Attentional Network for Weakly-Supervised Learning                                |
|   CVPR19   |      CMCS     | Completeness Modeling and Context Separation for Weakly Supervised Temporal Action Localization        |
|   ICCV19   |               | Weakly-supervised Action Localization with Background Modeling                                         |
|   ICCV19   |               | Weakly Supervised Temporal Action Localization Through Contrast Based Evaluation Networks              |
|   ICCV19   |     3C-Net    | 3C-Net: Category Count and Center Loss for Weakly-Supervised Action Localization                       |
|   AAAI20   |     BasNet    | Background Suppression Network forWeakly-supervised Temporal Action Localization                       |
