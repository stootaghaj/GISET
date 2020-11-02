# GISET
## Gaming Image Quality Dataset
 
GISET is a gaming image quality dataset that is created based on extracted frames of gaming videos. For the creation of the dataset, we conducted a subjective test with 20 valid participants. For the assessment of the image quality, a discrete 5-point scale, Hidden Reference Absolute Category Rating (HR-ACR) method, was used.

The frames are extracted from encoded and raw video sequences that are included in the dataset. 
Link:
https://drive.google.com/open?id=1R2MDH6aNmhZwXFwdHmM91kGIxwR3krf5

The dataset has four folders as follows:

1.	Subject Ratings: subjective ratings together with additional pre/post-game ratings. Raw subjective rating will be realized upon acceptance of the paper. 

2.	MOS: The Mean Opinion Score (MOS) information is provided together with some plots lined to MOS ratings.   - Image Quality in 5-point ACR scale (VQ_EC)
 

3.	Plots and Metrics: the results of objective metrics are provided together with some scatter plots of each metric and subjective results (some results will be released upon acceptance of the paper).

4.	Materials: the raw reference frames and encoded frames are provided in PNG format.

## Selection of Content

With the aim to only keep the relevant distortions of H.264/AVC compression for gaming content, we decided to extract the frames directly from an existing gaming video dataset, GVSET. Thus, a dataset was built consisting of 164 frames chosen from GVSET in which for each source image, we selected three encoded images with different levels of quality. Among the three encoded images, one was extracted from a video with low bitrate level, aiming at the blockiness artifacts, and one with lower resolutions than source image with the aim to trigger the blur in the frame and finally one with a mixture of both artifacts. It has to be noted that in GVSET all encoded videos with resolution lower than 1080p are upscaled to 1080p using bicubic filter which leads to blur artefact. The source frames are selected from multiple video games from different parts of each sequence. We tried to choose an appropriate distribution of distortions by considering their VMAF quality levels . 
The level of distortion for each frame was selected based on the VMAF values within a specific range from 20 to 80. The upper bound of VMAF of 80, was chosen based on the our previous works which found no significant difference between reference condition and encoded videos with VMAF value above 90 in subjective ratings. In addition, we tried to include all types of frames (I, B, P), since in I-frames, typically blockiness is not dominant compared to B and P frames.

## Test Methodology

In order to get insights on the influence of encoding parameters on the perceived video quality, we assess different types of degradation using the dimension-based subjective quality evaluation that is designed for video telephony, describing the identification of relevant perceptual video quality dimensions. While this method was proposed for a video-telephony experiment, we found it a suitable method to identify the types of degradation for image content as well. Therefore, we added two questions in order to assess  Fragmentation and Unclearness in addition to overall image quality. Fragmentation is defined by synonyms such as fallen apart, torn and blocky which was only triggered by a low bitrate in our dataset. Unclearness is defined by synonyms such as unclear, blur and smeared image which is triggered by lower resolution due to upscaling artefacts. 

Each dimension is explained to the participants in an introduction in a written form using describing adjectives and in form of example videos. The rating scales are designed based on Likert-Scales, using the antonym pairs to describe the range of the scales. However, we used the 5-point ACR scale for video quality, fragmentation and unclearness, in order to be consistent with typical video quality tests as well as with the ratings of GVSET. 


## Citation 
Please cite the paper below if you use the dataset:
```
	@inproceedings{NDNetgaming,
		title={{NDNetGaming - Development of a No-Reference Deep CNN for Gaming Video Quality Prediction}},
		author={Utke, Markus and Zadtootaghaj, Saman and Schmidt, Steven and Bosse, Sebastian and Moeller, Sebastian  },
		booktitle={Multimedia Tools and Applications},
		year={2020},
		organization={Springer},
	  }
```


