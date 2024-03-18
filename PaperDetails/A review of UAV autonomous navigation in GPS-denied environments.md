---
date: 2023
link: https://www.sciencedirect.com/science/article/pii/S0921889023001720
Keyword: Optical flow, 
---

## Summary
This paper proposes a taxonomy which firstly classifies the navigation strategies into Mapless and Map-based ones based on map usage and then, respectively categorizes the Mapless navigation into Integrated, Direct and Indirect approaches via common characteristics. The Map-based navigation is then split into Known Map/Spaces and Map-building via prior knowledge.

![](../Image/A%20review%20of%20UAV%20autonomous%20navigation%20in%20GPS-denied%20environments.png)

- **Mapless category**: usually does not need any prior knowledge of the environment but rather perceive the environment as they navigate it without creating any maps during navigation
![](../Image/A%20review%20of%20UAV%20autonomous%20navigation%20in%20GPS-denied%20environments%203.png)
    - **Non-distance Perceptron**: processes sensor data to obtain different Non- distance representations
    - **Distance Perceptron**: Distance representations from sensor data
    - **Control Unit**: process Non-distance representations or Distance Perceptron to output UAV commands
    - **1-2-7 Integrated Approaches**: There is no independent Control Unit in these approaches, that is, the Control Unit is integrated within the entire algorithm. The Non-distance representations of these approaches are less correlated with environments but directly corresponded to the UAV control. For example, a CNN acts as an encoder which extracts the sensor data and directly outputs UAV control commands (e.g., steering and speed).
        - CNN based Supervised Learning : 
            - Annotation, e.g. ‘Non-collision’ and ‘Collision’ classes depending on whether the distance to collision is smaller than specific distance and traing CNN(Drawback: requires a large number of images with relevant and accurate labels for training)
        - Reinforcement Learning: 
            - Discrete commands(forward, left, right, up, and dow): combining a conditional generative adversarial network (cGAN), a deep Q learning network and a recurrent network to directly output UAV commands.
                - cGAN to generate the depth maps from RGB images 
                - feeds 𝑙 generated depth maps simultaneously into 𝑙 streams deep Q-learning network
                - followed by a recurrent network layer for temporal attention and outputted optimal Q-value for desire state action
            - Continuous commands(quantity of movement in various directions): 
                - pretrained the Convolutional Variational encoder (a encoder–decoder structure) to turn the RGB images into depth images
                - use the latent features extracted from the encoder as current State 𝑆𝑡 with collision and non-collision rewards to train the Reinforcement Learning model.
    - **1-2-4-7 Direct Approaches**: the Non-distance representations are nor- mally extracted from the Field of View (FOV) based on CNN or OF algorithms and more relevant with **environments** but less correspond to the UAV control such as relative positions in corridors and OF differences. Therefore, these approaches require an independent Control Unit as the Decision Tree to directly map the environmental representations to the UAV Commands.
        - CNN-based extraction: 
            - DenseNet-161 as the backbone CNN model and modified the outputs of the last latent layer with four nodes which respectively inferred as 𝐶 𝑒𝑛𝑡𝑒𝑟, 𝐿𝑒𝑓 𝑡, 𝑅𝑖𝑔h𝑡 and 𝐸𝑛𝑑 of corridor positions; Control Unit receives the classification results to control the UAV shifting away from the side walls and flying along the center of the corridor
            - By combining the genetic algorithm with Deep CNN which encodes the hyperparameters as genes, a DCNN- GA which firstly adjusted the hyperparameters of VGG-16 during training and then, transferred the last five layers of VGG-16 by stacking them after the Xception model to predict the angle 𝜃.
        - Optical Flow based extraction: the movements of pixels due to the relative motions between the camera and scenes
            - The OF features extracted by the OF-based Magnitude Estimation which enables the Control Unit to directly adjust orientation based on the difference of OF magnitudes on the left and right side (𝑂𝐹𝐿, 𝑂𝐹𝑅) of FOV.
    - **1-3-4-7 Indirect Approaches**: In order to achieve **precise control**, the Distance representations of these approaches are usually extracted from Distance Perceptron and formulated as a distance matrix. The Control Unit summarizes these large amounts of distance information and outputs the UAV Commands. Therefore, the strategies using Distance representations (e.g., CNN-based, OF-based and Reflection-based Distance Estimation) are classified as Indirect Approaches.(Both the CNN and OF algorithms provide distance estimation from captured input images while the distances detected from Reflection-based sensors such as Infrared, Ultrasonic, and Laser are fused and estimated.)
        - CNN-based distance estimation
            - CNN-based Distance Estimation: get the depth maps from images
            - CNN-based object detection: YOLO v3 to only identify the useful indoor structures such as corridor intersections and since the different distances to the objects lead to different bounding boxes’ dimensions, the Control Unit regresses the bounding boxes’ dimension to real-world distances.
        - OF-based distance estimation
            - OF magnitudes compensated by IMU data can be used to estimate the distance
            - without using IMU(inertial sensors), combined EdgeFlow and EdgeStereo
        - Reflection-based distance estimation
            - ultrasonic liked sensors: the surrounding distances to obstacles are directly collected within the limited range. To compensate the limitations of shorter range and surfaces which may absorb the signals like clothes and textiles,  a series of Kalman Filter in the Control Unit are used to fuse Infrared and Ultrasonic sensors. since these Ultrasonic/Infrared sensors only return the frontal distances without relative directions to the UAV, there is no steering commands to navigate through the obstacles
            - LiDAR: which provides distances along with corresponding directions with a wide range of FOV can be used to overcome the drawback of ultrasonicliked sensors



- **Map-based**: requires the metrical or topological representations of environments and consists of **Obstacle Mapping**, **Self-localization** and **Path Planning** sub components which are usually independent to each other
![](../Image/A%20review%20of%20UAV%20autonomous%20navigation%20in%20GPS-denied%20environments%202.png)
    - **Known Map or Space**: The strategies have **prior** spatial details about the environments such as the positions of access points, start and destinations, obstacles or even the entire maps before navigation which is followed by UAV Self-localization and Path Planning.
        - it is not always necessary to reconstruct the maps during navigation, but the UAV Self-localization technologies such as Visual Odometry (VO), Landmark and Radio Frequency-based (RF-based) localization of the existing complete UAV navigation strategies are required.
        - VO(a process which compares the current and the previous visual observed from a single or multiple cameras to analyze differences in egomotion (i.e., egomotion estimation or pose estimation)): 
            - Feature-based(invariant feature descriptors): e.g. feature detector, feature matching in sequential images and frame-to-frame pose estimation
            - Direct Methods(estimates motions directly from intensity values)
        - Landmark
            - Landmarks with specific representations that are dif- ferent from the background in the FOV
            - e.g. use roof landmark pat- terns as waypoints by comparing with stored features in database for UAV’s drifting correction during point-to-point navigation 
            - e.g. Apart from matching features in database, the CNN-based object detection, SSD Inception V2 was used to detect the QR code as landmarks which contain coordinate information for the UAV’s calibration
        - RF-based
            - The communication infrastructures that can transmit and receive RF signals such as WiFi access points and cellular towers are installed in many urban environments. The calculations based on Radio Signal Strength Indicator (RSSI) and Time difference of Arrival enable distance measurements in GPS-denied environments


    - **Map-building**: basically it is SLAM-based navigation which was defined as **simultaneous map building and localization** during navigation without any prior information, constructing local/global maps during navigation in totally unknown areas
        - V-SLAM(e.g. monocular SLAM)
            - Feature-based(ORB-SLAM): extract and match key-points in two consecutive images. According to these matched key-points, minimiz- ing their reprojection errors (the pixel-position error between the projected pixel of the real-world 3D-point and the reprojected pixel 3D-point based on the current estimated pose) to estimate the camera pose and generate sparse 3D maps. 
            - Direct methods(LSD_SLAM): uses the image intensities to estimate the location and surrounding area. 
        - LiDAR-SLAM
            - calculates the time of flight of a laser to directly output the relative distance and position of obstacles, creating what are known as point clouds. If obstacle information and current vehicle location is known, local/global environments can be easily reconstructed.
            - Google’s Cartographer SLAM algorithm

    - **Path Planning**: 
        - Mapping and localization 
            - Goal-Direction: 
            - Self-Exploration: requires the discovery of the entire unknown spaces and the problem is considered to be fully solved when 𝑉𝑓𝑟𝑒𝑒 ∪ 𝑉𝑜𝑐𝑐 = 𝑉∖𝑉𝑟𝑒𝑠, where the 𝑉𝑓𝑟𝑒𝑒 ⊂ 𝑉, 𝑉𝑜𝑐𝑐 ⊂ 𝑉 and 𝑉𝑟𝑒𝑠 ⊂ 𝑉 respectively represent the free, occupied and residual areas of the entire 3D space 𝑉 ⊂ 𝑅3. 
                - Next Best View (NBV)
                    - consider the candidate waypoints within the range of entire known spaces including the current sensor measurement rather than just frontiers and then, calculate the comprehensive gain for selection.
                - Frontier-based methods
                    - Defining the 𝐹 𝑟𝑜𝑛𝑡𝑖𝑒𝑟𝑠 regions at the edges between the explored and unexplored areas as candidate waypoints; 
                    - Calculating the comprehensive gain of candidate waypoints containing benefit (e.g., information gain) and cost (e.g., path length) metrics; 
                    - Selecting the next waypoint from candidates with the best comprehensive gain.
        - Planners: find a point-to-point optimal path with collision avoidance
        ![](../Image/A%20review%20of%20UAV%20autonomous%20navigation%20in%20GPS-denied%20environments%204.png)
            - Graph-based Planning: a graph 𝐺 = (𝑉 , 𝐸) consists of a finite set 𝑉 of nodes (or vertexes) corresponding to pixels/voxels of original image and a finite set 𝐸 of edges connecting neighboring nodes. The Graph-based Planning includes Graph Searching and Graph Sampling algorithms, which the Graph Searching is responsible to search through a set of nodes (𝑉 ) on a graph or map (𝐺) for optimal path searching while the Graph Sampling algorithms usually sample the environment as a set of nodes (𝑉 ), or other forms, then map and search to find an optimal path
                - Graph Searching algorithm: if the nodes in the environments had been assigned such as using multiple regions with same size to represent nodes, the Graph Searching is responsible to plan an optimal path from start to goal: Dijkstra, A*, Theta, Lazy Theta and Jump Point Search (JPS) etc.
                - Graph Sampling algorithm: sample environments as a set of nodes, or other forms, then search to find an optimal path from start-to-goal 

            - Bio-inspired Planning: mimicking biological behaviors to deal with path planning and opti- mization
                - CNN-based Reinforcement learning
                    - Double Deep Q Network with two uniform CNN models (i.e., policy and target) which were fed with a local map around the agent and the global map simultaneously for immediate collision avoidance and general direction decision respectively. The system shows that the proposed strategy can plan a path to trade off the multi-objective of coverage path planning and data harvesting.
                - Ant Colony Optimization (ACO)
                    - iteratively tracking pheromone trails between way- points to find the optimal path solution
                    - a Multi- Colony optimization for knowledge sharing between colonies to avoid sub-optimal solutions for single ant colony
                - Genetic Algorithm (GA): global optimization
                    - encodes the feasible regions or waypoints in environments as genes to generate chromosomes, then calculates fitness values and selects two parents chromosomes (i.e., Parent 1 and Parent 2) from start to destination
                - Particle Swarm Optimization(PSO)
                    - To eliminate the requirements of encoding chromosome for GA and high sensitivity of swarm’s size for ACO, PSO adjusts the speed and position vectors of particles based on their own experiences (individual best) and swarm communications (global best) to seek the optimum values.

            

        



