5. Performance Evaluation 1
Find examples where the TTC estimate of the Lidar sensor does not seem plausible. Describe your observations and provide a sound argumentation why you think this happened.

Some LiDAR TTC wrong because of some outliers and some unstable points from preceding vehicle's front mirrors, those need to be filtered out. Here we adopt a larger shrinkFactor = 0.24, to get more reliable and stable lidar points. Then get more accurate results.

6. Performance Evaluation 2
Run several detector/descriptor combinations and look at the differences in TTC estimation. Find out which methods perform best and also include several examples where camera-based TTC estimation is way off. As with Lidar, describe your observations again and also look into potential reasons.

when get a robust clusterKptMatchesWithROI can get a stable TTC from Camera. if the result gets unstable, It's probably the worse keypoints matches.

The TOP3 detector/descriptor combinations as the best choice for our purpose of detecting keypoints on vehicles are: SHITOMASI/BRISK
SHITOMASI/BRIEF
SHITOMASI/ORB
