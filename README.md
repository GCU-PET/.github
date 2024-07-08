# Instroduction
PET stands for Pet Emotion Tracking,  
a service that uses a camera to assess the emotional state of a user's pets and provides information about it to the user.

# Motivation 
In recent years, with the increase in single-person households in Korea, pet adoptions have also been on the rise.     
And there is a growing interest in the emotions and well-being of companion animals.   
   
<img src="https://github.com/GCU-PET/PET_wiki/assets/127282538/d7836bd6-b811-4bcd-b290-1b33c85b827a.png" width="40%" height="40%">
<img src="https://github.com/GCU-PET/PET_wiki/assets/127282538/81444066-c74e-4f52-92d4-f9e213800f7a.png" width="40%" height="40%">
   
However, among the general population, there are not many individuals who can accurately understand the behavior and psychology of companion animals.   
As a result, people often install home cameras to check on their pets' well-being when they are not at home.    
However, simply installing a home camera does not necessarily lead to a quick recognition of any issues with the pet.   
    
***

Our team have decided to focus on analyzing the behavior of companion animals.    
We aim to develop a system that analyzes abnormal behaviors or emotions in pets and provides this information to pet owners through a mobile app.
 
# Techniques
<img src="https://github.com/GCU-PET/PET_wiki/assets/112566149/4114fb96-7983-4559-bcaa-b842bce73d24" width="40%" height="40%">

> Flask server (YOLOv8)
https://github.com/GCU-PET/flask/wiki/Flask-Wiki

# Overall Structure
The overall structure is as follows :    
* The camera transmits video information to the server, where the footage is analyzed to initially detect the presence of the companion animal.      
* Subsequently, the system classifies the observed behavior, compares it with previously analyzed data, and transmits the categorized status to the user through a mobile application.    
* In case of abnormal behavior, the system sends a notification to alert the user.   
    
***

<img width="512" alt="image" src="https://github.com/GCU-PET/PET_wiki/assets/127282538/49b648a6-7a2a-4ff1-84e6-592a9905d469">       
<img width="700" alt="image" src="https://github.com/GCU-PET/PET_wiki/assets/127282538/a44205b8-2eb9-4e12-95a0-2e8e441560fd">    
<img width="512" alt="image" src="https://github.com/GCU-PET/PET_wiki/assets/127282538/5e7c677a-b150-417d-93f7-0151c7f81875">
     
As shown in the above image,    
* Using a webcam, Node.js extracts images from animal (video) recognition every second (subject to modification later).    
* The images received by the Node.js server are classified using YOLOv8 and Flask to determine the posture or appearance of the animal.   
* The classified data is then stored on the server, and the stored data is made available for user verification through the app.  

# DEMO
https://www.youtube.com/watch?v=30CmUwYl45s
