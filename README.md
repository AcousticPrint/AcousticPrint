# AcousticPrint


## Team
* [Harini Kolamunna](https://dblp.org/pers/k/Kolamunna:Harini.html) 
* Junye Li, 
* Thilini Dahanayake, 
* [Suranga Seneviratne](https://www.sydney.edu.au/engineering/about/our-people/academic-staff/suranga-seneviratne.html)
* [Kanchana Thilakaratne](https://www.sydney.edu.au/engineering/about/our-people/academic-staff/kanchana-thilakarathna.html)
* [Albert Y. Zomaya](https://www.sydney.edu.au/engineering/about/our-people/academic-staff/albert-zomaya.html) 
* [Aruna Seneviratne](https://www.engineering.unsw.edu.au/electrical-engineering/professor-aruna-seneviratne) 


## Media
https://www.youtube.com/watch?v=s9kNu…


## Introduction
*AcousticPrint* generates signature acoustic profiles for different classes of drones by using machine learning technologies that is capable of identify an oncomming acoustic signal is from any of the known classes or an outlier. The overview of the system architecture is shown below.
![System](/Images/Overview.png)

## Dataset
The dataset we used in this project is available with the following headings.
1. DS1-Experimentally-Captured: 
    * Drone acoustic profiles collected experimentally with a RODE NTG4 shotgun directional microphone for five different classes of drones, rangingfrom amateur to professional drones, **Parrot Bebop 2**, **DJI MavicPro**, **DJI Phantom 4 Advanced Pro**, **DJI Spark**, **DJI Matrice 100**; 
    * Drones are flying around at 20m above ground and within a 50m radius;
    * Signals are sampled at 44.1kHz;
    * *Training* - 30s; *Validation* - 10s; *Test* - 10s; captured on 3 different sessions over 2 days.
1. DS1-YouTube-Sourced: 
    * Drone acoustic profiles scraped from YouTube videos.
    * Traces for **Autel EVO**, **DJI Inspire2**, **JME**, and **DJI MavicAir**. 
    * *Training* - 30s; *Validation* - 10s; *Test* - 10s; scraped from 3 different YouTube videos.
1. DS2: 
    * Non-Drone acoustic profiles collected experimentally and scraped from YouTube videos.
    * Scraped from YouTube videos - **Vehicle Sound in a Busy Road**; **Buzzing of Bees**; **Humans Talking**.
    * Experimentally collected - **Calm Environment** 
    * *Training* - 30s; *Validation* - 10s; *Test* - 10s; scraped from 3 different YouTube videos/ captured on 3 different sessions.
1. DS3: 
    * Online downloaded acoustic signals (from https://www.soundsnap.com/) that consist of various mechanical sound; 13 vehicle sounds and 2 drone sounds that werenot used in training.
    * *Test* - 10s; 
    


* *Training* and *Validation* samples are augmented with Amplitude scaling and frequency warping techniques. Each sample is scaled 5 times along in the time axis and in amplitude by two separate values selected for from a uniform distribution, U(0.8, 1.2).
