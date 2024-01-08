# 1. Overview
Welcome to the project titled "Development of Driving Cycles for Electric Buses using ML in Patna, India." 

A driving cycle (DC) is often characterised as a time series of speed of a vehicle, where extra directives and conditions may be used. 
It is a vital concept in analysing the speed pattern of automobile vehicles and also plays a a crucial role in the creation of new vehicles as well as in the assessment of vehicle attributes like emissions and energy consumption, optimizing powertrain design, energy storage management, and overall operational efficiency (evaluating the economic and environmental feasibility) of electric bus deployment.

This project showcases the utilization of machine learning techniques to construct accurate driving cycles that reflect real-world driving patterns of electric and CNG buses in the city of Patna.

# 2. Objective
Rapid adoption of electric buses as a means to reduce carbon emissions and achieve sustainable urban transportation has prompted the need for accurate driving cycles.

The primary goal of this project is to construct driving cycles that represent real-world driving patterns of electric and CNG buses in Patna and accurately capture the nuanced behavior of buses on urban and rural roads.

# 3. Methodology
This methodology delineates the systematic approach undertaken to craft precise driving cycles utilizing machine learning techniques, including clustering algorithms.

# Data Collection:
1000 km real-world data collection was undertaken from electric and CNG buses. VBOX sensors were employed to collect continuous vehicle positional and kinematic data at a high frequency (10 Hz). The collected data encompassed latitude, longitude, speed, acceleration, and other pertinent parameters. Data collection spanned weekdays from 9 AM to 8 PM, capturing diverse driving conditions.

# Data Preprocessing & Analysis:
Collected data underwent meticulous examination to detect and rectify anomalies such as speed spikes, negative speed data points, and signal loss. Trajectory data were then scrutinized to identify micro-trips, forming the foundation for driving cycle construction. VBOX Test Suite software was used to extract the data gathered by VBOX
Sport for pre-processing and analysis.

# K-means Clustering (Machine Learning)
The utilization of machine learning techniques ensured the driving cycle's adherence to real-world driving patterns and allowed for a less than 10% deviation from target statistics. The chosen driving cycle was selected by comparing the constructed driving cycles to target statistics derived from collected data. 

**Data Scaling:**

Driving characteristics, including average speed, acceleration, and deceleration, underwent scaling to the same range to prevent bias.

**Cluster Formation:**

A widely recognized machine learning algorithm (K-means Clustering) employed to group micro-trips based on driving characteristics, to segment data and identify distinct driving patterns. The algorithm iteratively assigned micro-trips to clusters, minimizing the sum of squared distances between data points and cluster centroids.

Micro-trips have been divided into four separate clusters, each with its own distinct characteristics and representing various traffic conditions

<img width="200" alt="image" src="https://github.com/pkpandeyiitp/Driving-Cycle-Development/assets/123129440/c3670cb6-a87a-4f79-adc2-f13d55bc636e">

<img width="300" alt="image" src="https://github.com/pkpandeyiitp/Driving-Cycle-Development/assets/123129440/227646de-9f97-4c40-a4ff-48b57e2e2b1d">

<img width="500" alt="image" src="https://github.com/pkpandeyiitp/Driving-Cycle-Development/assets/123129440/60ddeda0-e901-4ac1-8f75-e9266140133e">

**Optimal Cluster Selection:**

The Elbow Method was employed to identify the optimal number of clusters, ensuring meaningful grouping of micro-trips.

**Cluster-Centric Candidate Cycle:** 

Micro-trips closest to the centroid of each cluster were selected to constitute the candidate driving cycle. We picked the same proportion of microtrip for candidate cycle formation from a group, which has same proportion in original data. This approach guaranteed the representation of distinct driving patterns in the cycle. To determine how closely the candidate cycle parameters resemble those of the base cycle, they are compared. The fact that candidate cycle values almost exactly match base cycle parameters suggests that DC accurately captures the driving parameters of the research region.

**Final Driving Cycle construction**

In this stage we are choosing the optimal driving cycle out of the designed driving cycles. The final driving cycle was selected based on least error. Relative Error is calculated by taking the difference between calculated value and target value with respect to the target value. 
Relative Error % (RE) = (C−T)∗100/T 

# 4. Results and Conclusion
The results of the project reveal insights into the driving patterns of electric and CNG buses in Patna and candidate cycles with duration lengths varying from 1700-1900 seconds were established. Eventually, 1800 s DC for Patna is created. It was established that the designed driving cycle had a comparable distribution of driving circumstances in terms of the types of roads and traffic than was seen in actual operating settings. Additionally, the comparison with international driving cycles showcases the uniqueness of Patna's driving characteristics.

<img width="422" alt="image" src="https://github.com/pkpandeyiitp/Driving-Cycle-Development/assets/123129440/45590977-bfa4-4bc1-8447-86d458e05957">

# 5. Implications and Future Work
The driving cycle created has significant implications for optimizing electric bus operations, energy consumption, and urban transportation planning. Additionally, the study's findings may be used to analyses of the electrical grid, the economic and lifetime of Electric buses, in construction of regional emission factors and emission inventories, both of which are excellent tools and sources of information for Patna's integrated transportation quality management.

It can also be helpful for manufacturing considerations of new vehicles. The research Assessment of these buses' battery performance, energy use, emissions, and driving range can be done using the results of this study.

Future work could involve the integration of predictive modeling to anticipate driving patterns and optimize electric bus operations further.

# Contact Information
For any inquiries or collaborations related to this project, please feel free to contact [Piyush Pandey] at [pkpandey.iitp@gmail.com].
