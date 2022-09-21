# Real-time-COVID-norms-violation-detection-system-with-face-recognition-
COVID-19 has brought the world into stand still and this pandemic showcased some peculiar problems that needed to be addressed. The very first preventive measures undertaken were to wear mask and maintain social distance monitoring. In order to implement this in a super populous country like India the administration used very coercive steps. The objective of this project is to propose and implement solutions to detect violations made with respect to COVID violation norms; wearing masks and maintaining social distance monitoring at public places and corporate sectors. This paper focuses on real-time solution to help law abiding forces through recognizing faces of the violators. The proposed framework for COVID norms violator detection problem has four folds- Inspecting social distance monitoring, detecting face masks, recognizing faces of person without mask and putting the information related to violators into an interactive UI. Given an unconstrained/constrained video, the proposed social distance monitoring inspection module uses IPM Transformation and Height-Width comparison. Followed by detecting face masks for people not maintaining appropriate distance (around 6 meter as suggested by WHO) using YOLO v4 architecture. Once mask detecting algorithm identifies the violator it passes on to recognizing faces using face recognition library based on Convolutional Neural Network (CNN). Our proposed model of mask detection based on YOLO proved to be the effective with mAP (i.e. Mean Average Precision) of 0.9395 on YOLOv4 respectively. In order to reduce the overall complexity of the proposed framework, mask detection model was applied only to people not following appropriate  social distance monitoring and also Face Recognition is imposed to unmasked faces to send alert notification to the violators and display the details to the law administrator. Lastly a dashboard is made using R to visualize data and live plots regarding distribution of violators in the given video. The proposed model is suitable for crowded area and can be integrated on convoluted system where CCTV is placed at specific stature.  
