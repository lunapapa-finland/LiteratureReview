### Introduction

The realm of navigation, an essential facet of maritime operations, has evolved dramatically with the advent of autonomous technologies. Traditionally, navigation involves the process by which vessels determine their position, course, and distance traveled, a task that has relied heavily on the expertise of human navigators and the Global Positioning System (GPS). However, the shift towards autonomy introduces a paradigm where vessels, specifically Maritime Autonomous Surface Ships (MASS), navigate with minimal or no human intervention. This transition not only marks a significant leap in maritime technology but also poses unique challenges and opportunities, particularly in environments where GPS, a cornerstone of modern navigation, is compromised or unavailable.

Autonomous navigation is not a novelty restricted to the maritime domain. Its development spans various sectors, most notably in self-driving cars, where it has been embraced more widely due to the immediate benefits of increased safety and efficiency. These systems incorporate complex algorithms and sensor arrays to perceive their environment, make decisions, and navigate through it autonomously. However, the application of such technologies in the maritime sector presents distinct challenges, given the dynamic and often unpredictable nature of the marine environment.

In the heart of autonomous navigation systems lie two critical components: the situational awareness system and the decision-making system. The former plays a crucial role in accurately perceiving the surrounding environment and the vessel's condition, serving as the foundation upon which decisions are made. Data fusion, the process of integrating information from various sources to achieve more accurate, reliable, and comprehensive situational awareness, becomes pivotal. Traditionally, GPS data has been paramount in navigation for providing precise location information. Nevertheless, maritime navigation often leverages additional data sources, including the Automatic Identification System (AIS) and Dynamic Positioning (DP) systems, especially in semi-autonomous contexts.

Despite the reliance on GPS and other systems, there exist scenarios where GPS signals are obstructed or unavailable, such as coastal areas with natural or man-made signal impediments, congested harbors, or remote or hazardous locations like caves. These GPS-denied environments necessitate innovative approaches to ensure safe and efficient navigation for MASS, underscoring the importance of alternative data sources and technologies.

The objective of this four-year PhD research is to harness the existing experimental setups within our faculty, including boats and drones, to explore, understand, adapt, and potentially enhance AI-enabled navigation systems previously developed for autonomous vehicles (AVs) and unmanned aerial vehicles (UAVs) for application in maritime contexts. This endeavor aims not only to push the boundaries of autonomous maritime navigation in challenging environments but also to contribute to the broader field of autonomous systems research by addressing the critical issue of GPS-denied navigation.

### Research Aims

The overarching goal of this PhD research is to pioneer advanced solutions for autonomous navigation in GPS-denied environments, specifically tailored for Maritime Autonomous Surface Ships (MASS). This endeavor is not only ambitious but also critical, given the increasing reliance on autonomous systems in the maritime domain and the inherent challenges presented by environments where traditional navigation aids like GPS are unreliable or unavailable. The research aims to address several key objectives:

1. **Enhance Situational Awareness**: Develop and refine methods for situational awareness that do not depend on GPS data, leveraging alternative data sources and sensor fusion techniques. This involves creating a comprehensive understanding of the environment and the ship's status, which is vital for safe and efficient navigation.

2. **Advance Decision-making Capabilities**: Integrate improved decision-making systems that can operate effectively in the absence of GPS, ensuring that autonomous maritime vessels can make informed, reliable, and safe navigation decisions in real-time.

3. **Innovate Data Fusion Methodologies**: Investigate and enhance data fusion methodologies that can integrate disparate data sources to provide accurate and reliable situational awareness. This includes exploring the use of AIS, radar, lidar, optical imaging, and other sensors as part of a multi-modal data fusion approach.

4. **Empirical Testing and Validation**: Utilize the faculty's existing experimental setups, including boats and drones, to empirically test and validate the developed autonomous navigation systems. This hands-on approach will not only provide practical insights but also ground the research in real-world applicability.

5. **Cross-Domain Technology Transfer**: Study, adapt, and potentially improve upon AI-enabled navigation systems previously developed for autonomous vehicles (AVs) and unmanned aerial vehicles (UAVs), for maritime use. This involves transferring and customizing technologies across domains to address the unique challenges of maritime navigation.

By achieving these objectives, the research aims to make significant contributions to the field of autonomous navigation, particularly in enhancing the capabilities and safety of MASS in environments where traditional navigation systems are compromised. This would mark a significant step forward in the autonomy of maritime vessels, opening new frontiers for exploration, commercial operations, and safety at sea.

### Literature Review

The concept of autonomous navigation, while increasingly becoming a cornerstone in various domains, presents unique challenges and opportunities when applied to the maritime sector, especially under the constraints of GPS-denied environments. This literature review delves into the current state of autonomous navigation technologies, the critical components that make up these systems, the use of data fusion in enhancing situational awareness, and the specific challenges faced in maritime navigation without GPS.

#### Autonomous Navigation Systems in Various Domains

Autonomous navigation has seen rapid advancements across multiple domains, notably in automotive and aerial drones, driven by the need for enhanced safety, efficiency, and operational capabilities. These systems rely heavily on a complex interplay of sensors, data processing, and AI algorithms to navigate through environments with varying degrees of autonomy. In the maritime context, the development of Maritime Autonomous Surface Ships (MASS) has been motivated by similar aspirations but is met with unique challenges due to the marine environment's complexity, such as dynamic sea states, varying weather conditions, and the presence of both static and dynamic obstacles.

#### Components of Autonomous Navigation Systems

Two primary components underpinning autonomous navigation systems are situational awareness and decision-making systems. **Situational awareness** involves the real-time perception of environmental and vessel state data, a task achieved through sensor inputs such as radar, lidar, cameras, and sonar. **Decision-making systems** interpret this data to navigate the vessel, making real-time decisions on course adjustments, speed changes, and obstacle avoidance. The effectiveness of decision-making is inherently tied to the quality and reliability of situational awareness, highlighting the importance of sophisticated data fusion techniques.

#### Data Fusion in Enhancing Situational Awareness

Data fusion is a critical process in autonomous navigation, integrating multiple data sources to create a comprehensive and accurate representation of the environment. In GPS-reliant systems, location data forms the backbone of navigational decisions. However, in GPS-denied scenarios, the emphasis shifts towards alternative data sources. The literature highlights various fusion algorithms and techniques designed to combine data from AIS, radar, optical sensors, and inertial navigation systems, aiming to maintain high levels of navigational accuracy and reliability in the absence of GPS.

#### Challenges in Maritime Navigation without GPS

Navigating without GPS poses significant challenges, particularly in maritime environments where alternative reference points may be limited. Coastal navigation, harbor maneuvers, and exploration in remote or hazardous areas exemplify situations where GPS signals are unreliable or non-existent. The literature explores innovative solutions and technologies that have been proposed or implemented to address these challenges, including vision-based navigation, the use of underwater acoustic beacons, and the integration of celestial navigation methods as part of a multi-modal approach to ensure continuous and reliable navigation capabilities for MASS.

### Empirical Studies and Technological Advancements

Empirical research and technological advancements play a crucial role in transitioning theoretical frameworks into practical navigation solutions for MASS. Studies involving real-world trials, simulations, and comparative analyses of different navigational technologies provide valuable insights into their effectiveness, limitations, and areas for improvement. Specifically, research focusing on the adaptation and optimization of AI-enabled systems from AVs and UAVs to maritime applications offers promising avenues for enhancing autonomous navigation capabilities in GPS-denied environments.

### Research Questions and Hypotheses

The exploration of autonomous navigation for Maritime Autonomous Surface Ships (MASS) in GPS-denied environments raises several pivotal questions and hypotheses. These inquiries not only guide the research trajectory but also aim to fill existing gaps in knowledge and application. Below are the formulated research questions and corresponding hypotheses:

#### Research Questions

1. **How can autonomous navigation systems for MASS be effectively implemented in GPS-denied environments?**
   This question seeks to understand the broader implications of deploying autonomous navigation systems in environments where GPS, a traditionally integral component for navigation, is unavailable. It aims to explore alternative methods and technologies that can ensure reliable and safe navigation.

2. **What role does data fusion play in enhancing situational awareness for MASS without GPS data?**
   This question delves into the specifics of how data from various sensors and sources can be integrated to form a comprehensive understanding of the surrounding environment and the ship's status, particularly focusing on the challenges and solutions in the absence of GPS data.

#### Hypotheses

1. **Integrating advanced data fusion techniques improves the accuracy of situational awareness in GPS-denied environments.**
   This hypothesis posits that by employing sophisticated data fusion algorithms, which combine information from multiple sensors and data sources, the situational awareness of MASS can be significantly enhanced, compensating for the lack of GPS information.

2. **Autonomous navigation systems designed for GPS-denied environments enhance the safety and efficiency of MASS operations.**
   This hypothesis suggests that with the successful implementation of autonomous navigation systems capable of operating without GPS data, MASS can achieve higher levels of operational safety and efficiency, even in challenging navigational contexts.

These research questions and hypotheses will direct the subsequent phases of investigation, focusing on the development, integration, and empirical testing of autonomous navigation technologies for MASS. By addressing these questions and testing these hypotheses, the research aims to contribute valuable insights and advancements to the field of maritime autonomous navigation.

### Methodology Framework

The methodology framework for this research is designed to systematically address the research questions and test the hypotheses through a combination of theoretical investigation, experimental setups, and empirical analysis. This multifaceted approach will involve studying existing AI-enabled navigation systems, adapting these technologies for maritime applications, and conducting real-world experiments using the faculty's experimental setups, including boats and drones.

#### Theoretical Investigation and Technology Adaptation

1. **Literature and Technology Review**: An extensive review of current autonomous navigation technologies, with a focus on those developed for autonomous vehicles (AVs) and unmanned aerial vehicles (UAVs), to identify potential applications and adaptations for MASS in GPS-denied environments.

2. **Technology Adaptation**: Based on the review, specific technologies and algorithms that show promise for maritime adaptation will be selected. This will involve theoretical adaptation and simulation to assess feasibility and potential performance in maritime settings.

#### Experimental Setups

1. **Boat and Drone Utilization**: The existing boats and drones will serve as experimental platforms to test and refine the adapted navigation systems. These platforms offer a versatile and controlled environment to conduct experiments that mimic real-world scenarios.

2. **Sensor Integration and Data Collection**: Essential to the adaptation process is the integration of various sensors (e.g., radar, lidar, optical cameras) and data collection systems on the experimental platforms. This setup will facilitate the collection of environmental and navigational data necessary for situational awareness and decision-making processes.

3. **Data Fusion Experiments**: Experiments designed to test and refine data fusion algorithms will be conducted. These experiments aim to integrate and analyze data from multiple sources to create a comprehensive situational awareness model without relying on GPS data.

#### Empirical Testing and Validation

1. **Real-World Trials**: Following the successful adaptation and preliminary testing, the navigation systems will be subjected to real-world trials under GPS-denied conditions. These trials will assess the systems' effectiveness in ensuring safe and efficient navigation.

2. **Performance Analysis**: The performance of the autonomous navigation systems will be evaluated based on criteria such as accuracy of situational awareness, decision-making reliability, and overall system robustness in varying conditions.

3. **Comparative Analysis**: Where possible, the performance of the developed systems will be compared against existing navigation solutions to highlight improvements and identify areas for further enhancement.

#### Analytical Techniques

1. **Statistical Analysis**: Statistical methods will be employed to analyze the data collected during experiments and trials, providing insights into the reliability and performance of the navigation systems.

2. **AI and Machine Learning Algorithms**: Advanced algorithms will be used both in the adaptation of navigation technologies and in the analysis of experimental data to identify patterns, optimize system performance, and improve decision-making processes.

This methodology framework lays the groundwork for addressing the research questions and hypotheses, aiming to advance the field of autonomous navigation for MASS in GPS-denied environments. The combination of theoretical research, technology adaptation, experimental validation, and analytical rigor is designed to yield empirical contributions that enhance the safety and efficiency of maritime operations.

### Anticipated Outcomes and Empirical Contribution

This PhD research is poised to make significant empirical contributions to the field of autonomous navigation for Maritime Autonomous Surface Ships (MASS), particularly in challenging GPS-denied environments. Through a rigorous methodology that encompasses theoretical investigation, technology adaptation, and empirical testing, the research aims to yield several key outcomes.

#### Development of Advanced Autonomous Navigation Systems

The primary anticipated outcome is the development and refinement of advanced autonomous navigation systems specifically designed for MASS operating in GPS-denied environments. These systems will integrate state-of-the-art data fusion techniques and decision-making algorithms to provide reliable and accurate situational awareness, enabling safe and efficient navigation without reliance on GPS.

#### Enhanced Situational Awareness through Data Fusion

A significant advancement expected from this research is the enhancement of situational awareness capabilities for MASS through innovative data fusion approaches. By effectively integrating data from a variety of sensors and sources, the research aims to create a comprehensive environmental and situational model that serves as the foundation for autonomous navigation decisions.

#### Empirical Validation of Autonomous Navigation Technologies

Another critical outcome will be the empirical validation of the adapted autonomous navigation technologies through real-world trials using boats and drones. These validations are expected to provide concrete evidence of the systems' effectiveness, showcasing their potential to improve maritime safety and operational efficiency.

#### Contributions to Maritime Navigation Safety and Efficiency

The research is anticipated to contribute substantially to the safety and efficiency of maritime navigation. By enabling MASS to navigate safely in GPS-denied environments, the developed technologies could significantly reduce the risk of accidents and enhance the capabilities of maritime operations in challenging conditions.

#### Cross-Domain Technological Insights

Furthermore, this research aims to offer valuable insights into the cross-domain adaptation of autonomous navigation technologies. By exploring and adapting solutions from the automotive and aerial domains to maritime settings, the research could pave the way for innovative cross-disciplinary approaches in autonomous systems development.

#### Empirical Contribution to the Field

Overall, the empirical contributions of this research will extend beyond the immediate advancements in autonomous navigation for MASS. By providing a robust framework for developing, testing, and validating navigation systems in GPS-denied environments, the research will contribute to the broader field of autonomous systems, offering insights, methodologies, and technologies that can be applied in various other domains facing similar challenges.

### Timeline and Milestones

This section outlines the proposed timeline and key milestones for the four-year PhD research on autonomous navigation for Maritime Autonomous Surface Ships (MASS) in GPS-denied environments. The timeline is structured to ensure a systematic approach to achieving the research objectives, allowing for the development, testing, and refinement of autonomous navigation systems.

#### Year 1: Foundation and Initial Development

- **Q1-Q2**
  - Literature review on autonomous navigation technologies, with a focus on maritime applications and GPS-denied navigation challenges.
  - Selection of technologies and algorithms from AVs and UAVs for adaptation to maritime settings.
- **Q3-Q4**
  - Initial adaptation and simulation of selected technologies for maritime use.
  - Development of experimental setups using boats and drones, including sensor integration.

**Milestone**: Completion of literature review and preliminary technology adaptation plan.

#### Year 2: Experimental Development and Testing

- **Q1-Q2**
  - Implementation of data fusion algorithms and integration of situational awareness systems on experimental platforms.
  - Preliminary testing in controlled environments to assess system performance and reliability.
- **Q3-Q4**
  - Refinement of navigation systems based on preliminary testing results.
  - Extended testing under varied conditions to evaluate system adaptability and robustness.

**Milestone**: Establishment of functional autonomous navigation systems on experimental platforms.

#### Year 3: Real-World Trials and Analysis

- **Q1-Q2**
  - Conducting real-world trials of autonomous navigation systems in GPS-denied environments using boats and drones.
  - Collection of comprehensive performance data.
- **Q3-Q4**
  - Data analysis and performance evaluation of navigation systems.
  - Identification and implementation of necessary refinements and optimizations.

**Milestone**: Empirical validation of autonomous navigation systems in real-world settings.

#### Year 4: Finalization and Dissemination

- **Q1-Q2**
  - Final system refinements based on comprehensive analysis and feedback from Year 3 trials.
  - Preparation of case studies and research findings for publication.
- **Q3-Q4**
  - Dissertation writing, focusing on research findings, technological contributions, and implications for future research.
  - Presentation of research outcomes at conferences and submission of findings to academic journals.

**Milestone**: Completion of PhD dissertation and dissemination of research findings to the academic and professional community.









Your research plan is comprehensive and well-articulated, focusing on an innovative area within maritime navigation. To refine it further, I'll offer adjustments for clarity, conciseness, and flow, ensuring your objectives are vividly and systematically presented. Here's a refined version:

---

## Research Plan for PhD Application: Exploring Autonomous Navigation Strategies for GPS-Denied Environments in Maritime Autonomous Surface Ships (MASS)

### Introduction and Research Aims

In January 2017, the Maritime Safety Committee (MSC) recognized the burgeoning field of autonomous ships, marking a pivotal shift towards autonomous navigation solutions [1]. Traditional maritime navigation, reliant on human expertise and the Global Navigation Satellite System (GNSS) integrated with Dynamic Positioning (DP) systems, is evolving. The advent of sensor fusion and artificial intelligence (AI) technologies heralds a new era where Maritime Autonomous Surface Ships (MASS) can operate independently, minimizing or eliminating human intervention [2].

However, GPS-reliant systems face challenges in environments where signals are compromised, such as in coastal areas with signal obstructions, congested harbors, or remote and hazardous locations. These scenarios underscore the need for innovative navigation strategies that ensure operational safety and efficiency without relying on GPS.

Building on the advancements in autonomous vehicles (AVs) and Unmanned Aerial Vehicles (UAVs), this four-year PhD research aims to adapt and enhance AI-enabled navigation systems for MASS, tackling the unique challenges of GPS-denied environments. The project seeks to advance maritime navigation technologies, contributing significantly to autonomous systems research by addressing the critical issue of GPS-denied navigation.

#### Research Objectives

1. **Cross-Domain Technology Transfer:** Adapt and customize AV and UAV navigation technologies for maritime applications, addressing the specific challenges of the maritime environment.

2. **Enhance Situational Awareness:** Develop methods to improve situational awareness without GPS data, utilizing alternative data sources and sensor fusion techniques, including lidar, cameras, and IMUs, as part of a comprehensive multi-modal data fusion strategy.

3. **Advance Decision-Making Capabilities:** Incorporate advanced AI models for object detection, obstacle avoidance, simultaneous map building and localization (SLAM), and path planning. These enhancements will enable MASS to make informed, reliable, and safe navigation decisions in real-time, even in the absence of GPS.

4. **Empirical Testing and Validation:** Leverage the faculty's experimental setups, including boats and drones, to empirically test and validate the developed navigation systems. This practical approach will ground the research in real-world applications, providing valuable insights into the system's performance and effectiveness.

Through these objectives, the research aims not only to pioneer advancements in autonomous maritime navigation but also to contribute broadly to the field of autonomous systems, particularly in overcoming the challenges of navigating without GPS. 

---

This version refines the structure and clarity of your original plan, emphasizing your research's innovation and its contribution to the field.




The realm of navigation, a crucial aspect of maritime operations, is undergoing evolution towards seeking autonomous solutions, spurred by the Maritime Safety Committee's (MSC) decision to include the issue of autonomous ships on its agenda in January 2017 [1]. Traditionally, navigation involves vessels determining their position, course, and distance traveled, relying heavily on human navigators' expertise and the Global Navigation Satellite System (GNSS) integrated with Dynamic Positioning (DP) systems. However, with the shift towards autonomy, there is a paradigm shift facilitated by the integration of sensor fusion and artificial intelligence capabilities. This shift allows Maritime Autonomous Surface Ships (MASS) to operate with minimal or no human intervention [2]. 

  

Despite the reliance on GPS and other systems such as the Automatic Identification System (AIS) and Dynamic Positioning (DP), there are scenarios where GPS signals are obstructed or unavailable. These scenarios, such as coastal areas with natural signal impediments, congested harbors with signal interference, multipath effects, or remote and hazardous locations like cave rescues or surveys, present unique challenges and opportunities for autonomous navigation where GPS, a cornerstone of modern navigation, is compromised or unavailable. 

  

Thanks to rapid developments in academia and industry, particularly in autonomous vehicles (AVs) and Unmanned Aerial Vehicles (UAVs), extensive work has been done and can be explored in detail. The overarching goal of this four-year PhD research is to investigate, understand, adapt, and potentially enhance AI-enabled navigation systems previously developed for AVs and UAVs, to tailor for Maritime Autonomous Surface Ships (MASS). This endeavour aims not only to advance autonomous maritime navigation in challenging environments but also to contribute to the broader field of autonomous systems research by addressing the critical issue of GPS-denied navigation.  

The research aims to address several key objectives: 

Cross-Domain Technology Transfer: This involves transferring and customizing technologies across domains to address the unique challenges of maritime navigation. 

Enhance Situational Awareness: Develop and refine methods for situational awareness that do not depend on GPS data, leveraging alternative data sources and sensor fusion techniques with lidar, camara, IMU and other sensors as part of a multi-modal data fusion approach. This involves creating a comprehensive understanding of the environment and the ship's status, which is vital for safe and efficient navigation. 

Advance Decision-making Capabilities: Integrate improved decision-making AI models in the area of object detection, obstable avoidance, simultaneous map building and localization(SLAM) generation and path planning that can operate effectively in the absence of GPS, ensuring that autonomous maritime vessels can make informed, reliable, and safe navigation decisions in real-time. 

Empirical Testing and Validation: Utilize the faculty's existing experimental setups, including boats and drones, to empirically test and validate the developed autonomous navigation systems. This hands-on approach will not only provide practical insights but also ground the research in real-world applicability. 