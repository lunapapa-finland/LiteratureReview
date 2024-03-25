---
date: 2022
link: https://ieeexplore.ieee.org/document/9207841

---

## Summary
THE Maritime Safety Committee (MSC) of the International Maritime Organization (IMO) defines a Maritime Autonomous Surface Ship (MASS) as “a ship which, to a varying degree, can operate independently of human interaction”. Although a vessel performs several operations simultaneously, here primarily on the problem of **sensing for autonomy in navigation** and **situational awareness** functions.

Autonomous systems consist of 
- perception
    - ship positioning
    - RADAR
    - other sensors that scan the environment
- control elements
    - propulsion(by using azimuth thruster) and steering systems
    - Global Navigation Satellite System (GNSS) integrated with Dynamic Positioning (DP) system

The key benefits of multi-sensor perception systems are increased availability and integrity through complementary sensing, that is, targets that cannot be detected with one sensor may be detectable with another sensor, and redundancy, that is, an observation can be cross-validated from different sources

We set out to review the relevant background research, equipment, and methods regarding the perception systems for autonomous ships. This includes reviewing the suitable sensors and artificial intelligence techniques. As there is yet little research done in this field, our approach is to cover also those works that appear to be outside of the main area of interest but that introduce methods that are likely to be useful in constructing multi-sensor perception systems for maritime environments.

Maritime context has received less attention on multi-sensor perception systems: Maritime weather is harsh, The harsh weather makes the maritime environment less attractive for initial sensor research, as the sensor systems need be developed beyond the first experimental phases in order to be weather- proof

Autonomous vessel research and projects have had a con- siderable concentration in North Europe and more specifically Norway and Finland. The best-known endeavours include the MUNIN project [14], the AAWA project [11], the Finnish OneSea Ecosystem2 with its Jaakonmeri test area, the Norwegian Yara Birkeland3, SIMAROS, AUTOSEA [15] and ROMAS projects, the Chinese Unmanned Cargo Ship Development Alliance (UCSDA) and test areas, Japanese NYK’s plans for remote operation, and Singaporean endeavors related to autonomous maritime operations.

###  REQUIREMENTS FOR SITUATIONAL AWARENESS IN AUTONOMOUS VESSELS(operational requirements from background literature)
The captains tend to do continuous cross-referencing of the ship’s location based on RADAR targets, ECDIS screen (which derives its location from the DGNSS), and visual observation of the view outside of the ship. **This means that a similar functionality will be implemented also on autonomous vessels, that is, create a system which itself primarily distrusts any single data source and prioritises cross-referencing and verification of data from multiple sensors.**

- Requirement for Position-Navigation-Timing (PNT) 
- Requirement for Requirements for Sensing
- Requirements for AI/ML Software
The AI software and ML functions are used to fuse data from different sensors, process this data, provide target detec- tion and classification, analyse the data with regard to the operational requirements and perform an output of the results. The AI-function has therefore the following key requirements. It should have the ability to:
• work offline from the Internet, once properly trained locally or in the cloud,
• compute SA results in online mode within reasonable time (less than 60s),
• both detect and classify targets with reasonable accuracy (true and false positive, true and false negative),
• analyse input sensor and its own performance and result quality (integrity monitoring of sensor assembly),
• work with Commercial-Off-The-Shelf (COTS) hardware as well as custom equipment,
• output data in a suitable format.
###  REVIEW OF SENSORS FOR AUTONOMOUS VESSELS
#### Proposed Architecture for the Experimental Sensor Assembly
visual (cameras), remote sensing (RADAR and LiDAR), audio (microphones), and localization (satellite navigation and Inertial Navigation System (INS))
In addition, AIS broadcasts can be integrated along with maritime data from other external database
there are a number of other potential sen- sors which can be included here, for example, depth-sensor, 3-dimensional Sound Navigation and Ranging (SONAR), Radio Direction Finder (RDF), Automatic Dependent Surveil- lance – Broadcast (ADS-B), and visibility meter. Some of these sensors already exist on board many ships.

For sensor fusion, the detection zone can be divided into two regimes: 
(1) long range - from about 1 NM and above, where AIS, RADAR, and stereo cameras (in good weather conditions) are relevant

(2) close range - below 1 NM, where LiDAR, cameras, and microphones are applicable

The overall processing strategy in our suggested deployment is: (1) an object is detected at long range with conventional ship RADAR and can be matched against camera and AIS observations in terms of position, velocity, and heading, as stereo cameras enable the calculation of distances. (2) On close range, LiDAR is used in conjunction with AIS, cameras, and sound sensors. 

#### Sensors for Precise Absolute Positioning
Global Navigation Satellite Systems (GNSS) have become the primary source of position and timing information for the vessel bridge

**Position-Velocity-Time (PVT) solution**
However, a common technique to determine heading, roll, and pitch is to use an Inertial Measurement Unit (IMU) integrated with the GNSS receiver 
The standards used for interfacing the PVT data to a computer or a display unit are typically NMEA 0183 and its successor NMEA 2000 [25] developed by the National Marine Electronics Association. 
For example, using Real-Time Kinematic (RTK) is likely to be useful in port approaches where the vessel proximity to the land-based GNSS base station is within the recommended limits. [https://epncb.eu/](https://epncb.eu/)

#### RADAR and LiDAR
A significant difference between RADARs and LiDARs is in the spatial dispersion of the signal.
RADARs use relatively wide beam width antennas making it very difficult to distin- guish small structural details of the target.
Modern LiDARs, on the other hand, are almost exclusively based on lasers and consequently have very narrow and well collimated beams. The downside of LiDARs is that they are very susceptible to weather phenomena. For darker targets, the range decreases rapidly.

When considering LiDARs for maritime environment, in addition to the measuring range and angular resolution, of particular interest is the scanning pattern or the horizon- tal and vertical Field-of-View (FOV).

#### Visual Sensors
By visual sensors, we mean all sensors which capture at least a two-dimensional image, one similar to a human eye. These include RGB (Red-Green-Blue), monochrome, and infrared digital cameras. Digital cameras can be used for positioning, ranging, and object detection and classification, all of which are essential tasks for an autonomous system

However, we note that in open sea conditions, there are no landmarks to perform camera-based positioning.

Ranging with cameras is usually done with a stereo camera setup, where the two cameras used and the target form a triangle. Otherwise, monocular distance estimation methods exploit the camera movement, but these methods can only estimate the distance to static targets

Ranging With Stereo Cameras: A stereo camera consists of two (monocular) cameras

in ideal maritime conditions, color cameras are better suited for detection and classification of objects, but in non-ideal conditions monochrome cameras are likely to be better for that.

Infrared (IR) cameras sense thermal radiation. This makes them an interesting choice in maritime conditions because most objects of interest, such as ships and humans, have very different temperature compared to water. 

Fusing cameras with RADAR and AIS, such as in [39], [40], appears as an attractive goal. 

#### Audio Sensors
Microphones, and especially microphone arrays, have the potential to provide valuable information for context awareness in maritime applications. Different types of vessels could be detected, classified, localized and tracked by analyzing the sounds that they produce, such as those from motors (e.g., propulsion, ventilation, cranes) and whistles. 

As an example of a commercially available solution, Rion’s Aircraft Noise Monitoring System uses a four element microphone array mounted in the same mast to detect and estimate the direction of arrival of the aircraft’s sound

#### AIS Receivers
Automatic Identification System (AIS) is a Very High Frequency (VHF) system used for broadcasting the location of vessels, fixed and floating Aids to Navigation (AtoN), or other obstacles in the sea such as oil platforms and wind farms 

 In addition to the location, AIS messages may also contain the vessel’s dynamic information, static information, and voyage related information.

 #### Public Maritime Datasets
there is a sufficient dataset for maritime, check the paper

### REVIEW OF AI TECHNIQUES FOR AUTONOMOUS VESSELS
situational abnormality detection, vessel classifica- tion, and localization. 
#### Key Requirements of AI for Maritime Problems
As stated previously, safety is the key in autonomous maritime systems, and thus the algorithms need to be robust in diverse operational situations. 
The Probably Approximately Correct (PAC) framework states that we could achieve better generalisation performance of a certain model with larger training dataset.  However, it requires the algorithms to be able to examine large-scale data, which might be problematic in many cases 

 A dataset is considered large-scale when the dimensionality of data record or the number of records is large.
1. Deep learning methods can handle large amounts of data but may struggle with high-dimensional data.
2. Gaussian Processes are not limited by the dimension of the data but may face computational challenges with large datasets, which can be mitigated through techniques like state space modeling for temporal data.

In maritime scenarios, the type of data can vary a lot, which requires us to use different AI methods for different types of data. For example, the data of AIS or GNSS are typically low- dimensional with the number of observations accumulating typically at 1 Hz rate. With time, these data may become large. In this case, deep learning models, especially recurrent neural networks [74], might have better capabilities for the analysis of a ship’s trajectory.

For the maritime audio signals, the number of dimensions is large. For example, an audio piece with 44.1 kHz and 1 s length has 44100 dimensions. Instead, we could use, for example, Short Time Fourier Transform (STFT) to transform the audio signal into spectral domain and use the spectro-temporal representation (image) as data features [75], [76]. RGB or RGB-depth9 (RGB-D) images from camera(s) are challenging both in data dimension and quantity, however deep learning especially deep convolutional neural networks [77], have successfully been employed for such type of data.


For deep learning methods, the predictive distribution is not easy to obtain, because complicated hierarchy neural network functions are involved when taking the integral to obtain the posterior. However, in many cases, the Gaussian processes method can give the closed-form solution to the predictive distribution


Another requirement for machine learning algorithms is the capability of online and offline learning. As shown in Figure 6, the computation might need to be done in real-time or offline depending on different situations. For example, while learning to classify the objects can be done offline, when we localise the maritime objects from camera or microphones the estimation has to be done in real-time.

 A. Rakhlin, “Lecture notes: Online methods in machine learning,” Massachusetts Inst. Technol. (MIT), Cambridge, MA, USA, Tech. Rep., Feb. 2016.

Online learning methods learn from sensor data on the fly, for example Bayesian state-estimation methods [79] and online probabilistic machine learning methods [65], [72]. These methods are especially suited for learning dynamics and prediction models. 
While offline learning, which we refer to as batch supervised machine learning type of methods, requires predefined training data.

Based on the above requirements, the selected machine learning algorithms need to take into account the following aspects: scale of data, uncertainty of prediction, and need for online learning.

#### AI for Maritime Self-Situational Awareness
The application areas of AI methods in maritime naviga- tion and vessel situational awareness are identified as object identification, localization, and trajectory analysis.

N. Fridman et al., “KINGFISHER: Total maritime awareness system,” in Proc. 16th Conf. Auto. Agents MultiAgent Syst. (AAMS), 2017, pp. 1784–1786.

#### Maritime Object Detection and Classification

The term “objects” here refers to anything that manifests on the maritime landscape and is distinguishable from the background, for example, ships, sea birds, and motor boats. The aim is to detect or classify the objects in the sensor range of a vessel. Such tasks are usually performed using one or multiple cameras due to the advances of image processing techniques and implementation simplicity. Audio data can also be applied here for this purpose. Interestingly, we observed that it is actually very rarely studied for maritime applications. We argue that, due to the large proportion of background noise from the environment (e.g., rain, wind, sea waves, bird sounds, humans shouting, and own engine), using sound for the detection and classification of maritime objects would require additional signal conditioning. The main challenge of using image data for object detection is that the dimension of data is quite large.

Using classical CNNs directly is non-trivial, because the classical CNNs are designed for image classification, not for detecting/classifying multiple objects from an image. In prac- tice, small sliding window is applied to recursively search all area of a large image. The drawback is that it costs vast amount of computational efforts, and the size of sliding window must be determined beforehand. This is not always possible in the maritime scenario, because the size of objects in an image varies according to the distance. 
The Region Proposal Network (RPN) [80] is a potential candidate solving: S. Ren, K. He, R. Girshick, and J. Sun, “Faster R-CNN: Towards real- time object detection with region proposal networks,” in Proc. Adv. Neural Inf. Process. Syst. 28. Cambridge, MA, USA: MIT Press, 2015

the main difference between a classical CNN and RPN is the region proposal layer, which gives potential area of object manifestation. This significantly reduces the search area for objects in an image. It is particularly useful when objects (such as a small boat) cover just a very small amount of area in terms of pixels



#### Maritime Object Localisation by Sound
#### Maritime Trajectory Analysis

Ship trajectories are part of the measured data used in situ- ational awareness systems. Two of the most common sources of trajectory information are the ship’s AIS transponder and the ship’s own GNSS receiver