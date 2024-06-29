<a href="https://imgur.com/54Ue0mM"><img src="https://i.imgur.com//54Ue0mM.png" title="source: imgur.com" /></a>  

# Azure-ElasticSearch-Integration

This project envolves integrating and deploying a SIEM tool 'ElasticSearch' with-in Microsoft Azure in order to Streamline log management and real-time threat detection for quicker identification and response to security incidents, by analyzing log data and identifying vulnerabilities, we can take steps to improve our security posture and prevent future attacks.

In essence, these integrations provide a powerful and centralized platform for collecting, analyzing, and visualizing security-related data, empowering us to proactively monitor our environment and respond effectively to security threats.

# Objectives:

 - Combine logs from various Azure VMs into a single location (Elasticsearch on Azure).
 - Simplify log analysis and investigation by eliminating the need to search through individual logs from different systems.
 - Filebeat on Azure VMs collects logs in real-time.
 - Elasticsearch efficiently stores and analyzes these logs.
 - Kibana allows for real-time visualization of security events, enabling faster identification of potential threats.
 - Provides a consolidated view of security-related events across your Azure environment.
 - Enables proactive monitoring for suspicious activity live brute-force attacks.


# 1. Create an Elastic Cluster resource on Azure
   
   <a href="https://imgur.com/egAhZsT"><img src="https://i.imgur.com//egAhZsT.png" title="source: imgur.com" /></a>   

# 2. Open the created Elastic Cluster resource
   
   - Under 'Elastic deployment configuration' > Logs & metrics > Logs >
   - Select the boxes for 'Send subscription activity logs' and 'Send Azure resource logs for all defined resources' > Save

   <a href="https://imgur.com/RCzJyAS"><img src="https://i.imgur.com//RCzJyAS.png" title="source: imgur.com" /></a>   

# 3. Elastic Cluster resource 
   
   - Under 'Elastic deployment configuration' > Virtual machines
   - Select VM resouces > Install Extension 

   <a href="https://imgur.com/qOcdi43"><img src="https://i.imgur.com//qOcdi43.png" title="source: imgur.com" /></a>   

# 4. View Logs & Metrics for a resource
   
   - Elastic Cluster resource > Virtual machines >
   - Under 'View data' column Select 'Metrics'
   
   <a href="https://imgur.com/z9EdReP"><img src="https://i.imgur.com//z9EdReP.png" title="source: imgur.com" /></a>
  
   - Elastic Cluster resource > Virtual machines >
   - Under 'View data' column Select 'Logs'

   <a href="https://imgur.com/DJSWGLZ"><img src="https://i.imgur.com//DJSWGLZ.png" title="source: imgur.com" /></a>

# 5. View Kibana User Interface
  
   - Elastic Cluster resource > Overview > Deployment URL (Kibana)

   <a href="https://imgur.com/i3IsFsc"><img src="https://i.imgur.com//i3IsFsc.png" title="source: imgur.com" /></a>

   - Kibana > Security > Explore > Hosts

   <a href="https://imgur.com/onNlGn2"><img src="https://i.imgur.com//onNlGn2.png" title="source: imgur.com" /></a>   

# 6. Visualizing Live Attack Network Traffic
   
   - Kibana > Security > Explore > Network

   <a href="https://imgur.com/tc6zMDg"><img src="https://i.imgur.com//tc6zMDg.png" title="source: imgur.com" /></a>   

# 7. User Authentications Success/Fail
  
   - Kibana > Security > Explore > Users
   - Observe the number of 'Failed' SSH login authentications into my Linux VM in the last 30 days.
   - Indicative of a Brute force attack

 <a href="https://imgur.com/xEohiFa"><img src="https://i.imgur.com//xEohiFa.png" title="source: imgur.com" /></a>  

   - Observe the number of 'Failed' SSH login authentications into my Linux VM in one day.
   - Indicative of a Brute force attack 

 <a href="https://imgur.com/iDBHm61"><img src="https://i.imgur.com//iDBHm61.png" title="source: imgur.com" /></a>  

 # 8. Event logs from host machine
   
    - Kibana > Security > Explore > Hosts > Events
    - Multiple SSH login attempts from single IP
    - Threat actor used a number of user names on the brute force attack

 <a href="https://imgur.com/1obIeHL"><img src="https://i.imgur.com//1obIeHL.png" title="source: imgur.com" /></a>  
    
    - Closer look of a single event log details
   
 <a href="https://imgur.com/d66O1p8"><img src="https://i.imgur.com//d66O1p8.png" title="source: imgur.com" /></a>    

We will utilize Kibana, the visualization platform for Elasticsearch, to analyze and visualize the ingested logs in real-time. This will allow us to monitor for suspicious activity, including the simulated brute-force attack, and gain insights into potential security threats.
Project Benefits:

Centralized Log Management: Elasticsearch provides a centralized repository for logs from various sources, enabling efficient analysis and investigation.
Real-Time Threat Detection: Kibana allows for real-time visualization of security events, enabling faster response to potential threats.
Improved Security Posture: By simulating and monitoring a brute-force attack, we can improve our understanding of security vulnerabilities and implement necessary security measures.
Learning Outcomes:

Gain practical experience with deploying and configuring Elasticsearch on Azure.
Understand the functionality of Filebeat for log ingestion.
Learn how to utilize Kibana for security event visualization.
Simulate and analyze a real-world security attack scenario.

 
