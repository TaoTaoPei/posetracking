# Enhanced Keypoint Information and Pose-Weighted re-ID Features for Multi-Person Pose Estimation and Tracking
Multi-person pose estimation and tracking are crucial research directions in the field of artificial intelligence, with widespread applications in virtual reality, action recognition, and human-computer interaction. While existing pose tracking algorithms predominantly follow the top-down paradigm, they face challenges, such as pose occlusion and motion blur in complex scenes, leading to tracking inaccuracies. To address these challenges, we leverage enhanced keypoint information and pose-weighted re-identification (re-ID) features to improve the performance of multi-person pose estimation and tracking. Specifically, our proposed Decouple Heatmap Network (DHN) decouples heatmaps into keypoint confidence and position. The refined keypoint information are utilized to reconstruct occluded poses. For the pose tracking task, we introduce a more efficient pipeline founded on pose-weighted re-ID features. This pipeline integrates a Pose Embedding Network (PEN) to allocate weights to re-ID features and achieves the final pose tracking through a novel tracking matching algorithm.


## Comparison to the state-of-the-art multi-person pose estimation on the PoseTrack validation dataset

| Dataset           | Method                    | Head | Sho. | Elb. | Wri. | Hip  | Knee | Ank. | mAP (%) |
|-------------------|---------------------------|------|------|------|------|------|------|------|------|
| PoseTrack 2017    | Detect-and-track          | 72.8 | 75.6 | 65.3 | 54.3 | 63.5 | 60.9 | 51.8 | 64.1 |
|                   | STAF                      | 75.7 | 73.9 | 67.8 | 56.3 | 66.8 | 62.3 | 56.9 | 66.3 |
|                   | PoseFlow                  | 66.7 | 73.3 | 68.3 | 61.1 | 67.5 | 67.0 | 61.3 | 66.5 |
|                   | FastPose                  | 80.0 | 80.3 | 69.5 | 59.1 | 71.4 | 67.5 | 59.4 | 70.3 |
|                   | SimpleBaselines           | 81.7 | 83.4 | 80.0 | 72.4 | 75.3 | 74.8 | 67.1 | 76.7 |
|                   | HRNet                     | 82.1 | 83.6 | 80.4 | **73.3** | 75.5 | 75.3 | 68.5 | 77.3 |
|                   | TKMRNet                   | 85.3 | **88.2** | 79.5 | 71.6 | **76.9** | **76.9** | **73.1** | **79.5** |
|                   | **Ours**                      | **85.4** | 87.5 | **81.2** | 72.9 | 76.1 | 76.5 | 72.4 | 78.9 |
| PoseTrack 2018    | STAF                      | -    | -    | -    | 64.7 | -    | -    | 62.0 | 70.4 |
|                   | PoseFlow                  | 63.9 | 78.7 | 77.4 | 71.0 | 73.7 | 73.0 | 69.7 | 71.9 |
|                   | MDPN                      | 75.4 | 81.2 | 79.0 | 74.1 | 72.4 | 73.0 | 69.9 | 75.0 |
|                   | TKMRNet                   | -    | -    | -    | -    | -    | -    | -    | 76.7 |
|                   | PoseWarper                | 79.9 | 86.3 | 82.4 | 77.5 | **79.8** | 78.8 | 73.2 | 79.7 |
|                   | **Ours**                      | **80.7** | **87.2** | **83.1** | **78.0** | 78.9 | **79.9** | **74.9** | **80.4** |


## Comparison to the state-of-the-art multi-person pose tracking on the PoseTrack validation dataset
| Dataset        | Method                | Head | Sho. | Elb. | Wri. | Hip  | Knee | Ank. | MOTA (%) |
|-----------------|-----------------------|------|------|------|------|------|------|------|-------|
| PoseTrack2017   | Detect-and-Track      | 61.7 | 65.5 | 57.3 | 45.7 | 54.3 | 53.1 | 45.7 | 55.2  |
|                 | SimpleBaselines       | 73.9 | 75.9 | 63.7 | 56.1 | 65.5 | 65.1 | 53.5 | 65.4  |
|                 | PGPT                  | 75.4 | 77.3 | 69.4 | **71.5** | 65.8 | 67.2 | 59.0 | 68.4  |
|                 | CorrTrack             | -    | -    | -    | -    | -    | -    | -    | 68.3  |
|                 | STE                   | 78.7 | 79.2 | **71.2** | 61.1 | 74.5 | 69.7 | **64.5** | 71.8  |
|                 | TKMRNet               | **81.0** | 82.9 | 69.8 | 63.6 | 72.0 | 71.1 | 60.8 | 72.2  |
|                 | **Ours**                  | 80.9 | **83.8** | 69.2 | 62.7 | **74.5** | **71.9** | 63.2 | **72.3**  |
| PoseTrack2018   | LightTrack            | -    | -    | -    | -    | -    | -    | -    | 64.9  |
|                 | PGPT                  | -    | -    | -    | 72.3 | -    | -    | 72.2 | 67.1  |
|                 | CombDet               | 74.2 | 76.4 | 71.2 | 64.1 | 64.5 | 65.8 | 61.9 | 68.7  |
|                 | CorrTrack             | -    | -    | -    | -    | -    | -    | -    | 69.1  |
|                 | TKMRNet               | -    | -    | -    | -    | -    | -    | -    | 68.9  |
|                 | LDGNNTrack            | **74.3** | 77.6 | **71.4** | 64.3 | **65.6** | 66.7 | 61.7 | **69.2**  |
|                 | Ours                  | 73.5 | **78.4** | 71.3 | **65.2** | 64.1 | **67.8** | **62.7** | 69.0  |
