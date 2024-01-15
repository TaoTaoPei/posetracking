# Enhancing Multi-Person Pose Tracking: A Robust Strategy with Pose-Weighted Re-ID Features
This paper introduces the Decoupled Heatmap Module to effectively decouple the heatmaps generated from pose estimation, obtaining valuable keypoint information. Subsequently, a new Pose Construction Module is employed to reconstruct occluded poses. For the pose tracking task, we propose a more efficient pipeline based on re-identification (re-ID) features. This pipeline leverages the Pose-embedding Attention Mechanism to assign weights to re-ID features, mitigating interference from the background. Further, distinct matching strategies are employed for active and inactive trajectories, ensuring efficient and real-time tracking performance.


## Comparison to the state-of-the-art multi-person pose estimation on the PoseTrack validation dataset

| Dataset           | Method                    | Head | Sho. | Elb. | Wri. | Hip  | Knee | Ank. | mAP  |
|-------------------|---------------------------|------|------|------|------|------|------|------|------|
| PoseTrack 2017    | Detect-and-track          | 72.8 | 75.6 | 65.3 | 54.3 | 63.5 | 60.9 | 51.8 | 64.1 |
|                   | STAF                      | 75.7 | 73.9 | 67.8 | 56.3 | 66.8 | 62.3 | 56.9 | 66.3 |
|                   | PoseFlow                  | 66.7 | 73.3 | 68.3 | 61.1 | 67.5 | 67.0 | 61.3 | 66.5 |
|                   | FastPose                  | 80.0 | 80.3 | 69.5 | 59.1 | 71.4 | 67.5 | 59.4 | 70.3 |
|                   | SimpleBaselines           | 81.7 | 83.4 | 80.0 | 72.4 | 75.3 | 74.8 | 67.1 | 76.7 |
|                   | HRNet                     | 82.1 | 83.6 | 80.4 | 73.3 | 75.5 | 75.3 | 68.5 | 77.3 |
|                   | TKMRNet                   | 85.3 | 88.2 | 79.5 | 71.6 | 76.9 | 76.9 | 73.1 | 79.5 |
|                   | Ours                      | 85.4 | 87.5 | 81.2 | 72.9 | 76.1 | 76.5 | 72.4 | 78.9 |
| PoseTrack 2018    | STAF                      | -    | -    | -    | 64.7 | -    | -    | 62.0 | 70.4 |
|                   | PoseFlow                  | 63.9 | 78.7 | 77.4 | 71.0 | 73.7 | 73.0 | 69.7 | 71.9 |
|                   | MDPN                      | 75.4 | 81.2 | 79.0 | 74.1 | 72.4 | 73.0 | 69.9 | 75.0 |
|                   | TKMRNet                   | -    | -    | -    | -    | -    | -    | -    | 76.7 |
|                   | PoseWarper                | 79.9 | 86.3 | 82.4 | 77.5 | 79.8 | 78.8 | 73.2 | 79.7 |
|                   | Ours                      | 80.7 | 87.2 | 83.1 | 78.0 | 78.9 | 79.9 | 74.9 | 80.4 |





## Comparison to the state-of-the-art multi-person pose tracking on the PoseTrack validation dataset
