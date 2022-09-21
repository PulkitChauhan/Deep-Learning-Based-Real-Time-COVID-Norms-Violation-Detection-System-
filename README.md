# Deep Learning Based Real-Time COVID Norms Violation Detection System 
COVID-19 has brought the world into stand still and this pandemic showcased some peculiar problems that needed to be addressed. The very first preventive measures undertaken were to wear mask and maintain social distance monitoring. In order to implement this in a super populous country like India the administration used very coercive steps. The objective of this project is to propose and implement solutions to detect violations made with respect to COVID violation norms; wearing masks and maintaining social distance monitoring at public places and corporate sectors. This paper focuses on real-time solution to help law abiding forces through recognizing faces of the violators. The proposed framework for COVID norms violator detection problem has four folds- Inspecting social distance monitoring, detecting face masks, recognizing faces of person without mask and putting the information related to violators into an interactive UI. Given an unconstrained/constrained video, the proposed social distance monitoring inspection module uses IPM Transformation and Height-Width comparison. Followed by detecting face masks for people not maintaining appropriate distance (around 6 meter as suggested by WHO) using YOLO v4 architecture. Once mask detecting algorithm identifies the violator it passes on to recognizing faces using face recognition library based on Convolutional Neural Network (CNN). Our proposed model of mask detection based on YOLO proved to be the effective with mAP (i.e. Mean Average Precision) of 0.9395 on YOLOv4 respectively. In order to reduce the overall complexity of the proposed framework, mask detection model was applied only to people not following appropriate  social distance monitoring and also Face Recognition is imposed to unmasked faces to send alert notification to the violators and display the details to the law administrator. Lastly a dashboard is made using R to visualize data and live plots regarding distribution of violators in the given video. The proposed model is suitable for crowded area and can be integrated on convoluted system where CCTV is placed at specific stature.  

# Methodology 
In our study, we propose a 4-stage model including people detection, tracking social distancing, mask detection and face recognition for alerting violators as a total solution for zone-based monitoring in corporate sectors. The system is also suitable for crowded area and can be integrated on convoluted system where CCTV is placed at specific stature.
## 1. People Detection
Before Applying social distance monitoring algorithm, a pre-trained YOLOv3 people(human) detection model is used to detect humans. Original Model consists of more than 330K images out of which 200K are labelled on 80 different classes.
Original model : YOLOv3
Number of classes: 80
Dataset: COCO dataset (COCO is a large-scale object detection, segmentation, and captioning dataset)
Total images : 330 K (200 k labelled)
Classes: 80 
## 2. Tracking social distance
We are using IPM Transition and height-width comparison method as our social distancing algorithm.

## 3. Mask detection 
The dataset consists of 920 images for mask detection, gathered from Google, Bing and Kaggle datasets with specific images from MAFA dataset. 
![image](https://user-images.githubusercontent.com/43074750/191445413-797eed16-d606-4d8e-8b7b-1695c7eb9e8a.png)

# Hyper-parameters for mask detection

•	Learning Rate	0.001
•	Batch		64
•	Subdivisions	32
•	Steps		48001
•	Max Batches	6000
•	Epochs		548
•	Momentum	0.9
•	Decay		0.0006


# Conclusion
An efficient framework for the COVID norms violation system is proposed. Given a constrained and crowded video, the proposed framework detects the person not following predefined social distance and inspects the person for wearing a mask using the YOLOv4 model. The social distance monitoring method proposed is giving promising results on the IPM Transformation method and the Height-Width comparison method. Once the YOLO model detects the violator, the face recognition module identifies the person and sends the information to the law enforcement dept. In addition to that, our proposed framework aids the user to get information about the distribution of violators in a particular place. Our framework outperforms recent solutions like Prateek Khandelwal [14] with mAP (mAP @ 0.50 i.e. Mean Average Precision) of 0.9395 on YOLOv4. This system is very affordable and easy to deploy on real time surveillance on GPU. Once the model is trained and deployed, the only cost would be to maintain the hardware on which the model would be running. Hence, the system is suitable for the crowded area and can be integrated on convoluted system where CCTV is placed at a specific stature. 
