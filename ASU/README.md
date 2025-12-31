# ASU Report

## Summary

We evaluated the effectiveness of Instinct Environmental's Acoustic Surveying Unit 2 (ASU2) for American bullfrog (Rana catesbeiana; RACA) detection. The ASU2 was deployed with an open source BirdNET(V2.0.0) acoustic detection model onboard. As the name implies, the BirdNET model is focused on birds but also includes a handful of frogs, including RACA. With the BirdNET model onboard, the ASU2 hardware provides a timely analysis of recorded audio data to identify species. After the ASU2 analyzes the audio any positive identifications are relayed to a satellite and uploaded to Instinct Environmental’s web portal. The purpose of this project was to evaluate ASU2 hardware functionality for RACA detection under field conditions. The insights and lessons learned from this evaluation will guide future deployments of the ASU2 (or similar) hardware by The Nature Conservancy and their partners.&#x20;

This evaluation of the ASU2 was focused on hardware reliability, power consumption, satellite transmission reliability, and recording schedule guidelines. Note that an evaluation of the BirdNET model is outside of the scope of this work and would be redundant in nature. Peer reviewed research by Bota et al. (2024) demonstrated that the BirdNET model is highly effective for RACA detection.&#x20;

The overall results indicate that ASU2 reliably transmits positive detections of RACA in a field environment. Using our recommended recording schedule and settings, paired with a solar panel and battery, the ASU2 is expected to run for approximately 290 days without interruption. Because RACA are relatively sedentary during winter, deployment of the ASU2 from March to November can readily detect calling activity during breeding periods.&#x20;

Automated transmission of species identification results from the ASU2 greatly reduce the need for field work by eliminating regular memory card retrievals and remove the need to analyze audio data on local workstations. The near real-time information on invasive RACA presence, allows monitoring programs to adopt an early detection and rapid response paradigm to quickly stop new infestions before they spread. Labor hours that wouhd have previously focused on monitoring can now be shifted towards control activities.&#x20;

## Overview

(Please note that all field testing was conducted in an outdoor urban environment with call playbacks from recordings because we missed the RACA calling season).

During field testing, the ASU2 demonstrated excellent reliability with all RACA call playback bouts detected by the onboard hardware and successfully relayed to the satellite and the Instinct Environmental web portal. The ASU2 is projected to provide near real-time audio monitoring for nine months (296 days) without maintenance using the recommended schedule, detailed in the following section. The nine month limitation arises from the USB storage filling up. A data file of each audio recording is stored on the USB drive after it is analyzed and all files are saved, regardless of a positive detection or not. In case there is a need to review a specific audio file it can be retrieved manually by physically uploading the data from the usb drive. Note that the audio files themselves cannot be transmitted remotely to the web portal over satellite, only the detection results can be sent. Of course, if there is a need to extend the duration of recordings beyond nine months, a less frequent recording schedule will extend the time before the usb drive reaches capacity.&#x20;

The optional, but recommended, solar panel when paired with the system battery can hypothetically supply power indefinitely. However a regular maintenance schedule is reccomended to  inspect the panel, cables, and clean debris. &#x20;

The device is capable of uploading results within thirty minutes of a scheduled recording bout finishing - allowing rapid response to the presence of RACA within sensitive habitats. During testing we discovered that if bouts are spaced too close together they system stops functioning properly and recording and analysis will stop. The solution is to maintain at least one hour between recording bouts, this is refelcted in the reccomended schedule.&#x20;

A key limitation of the ASU2 is the inability of the device to make updates to the monitoring settings or schedule remotely. Because of this it is suggested that the schedule be carefully planned out to ensure that it meets the needs of the project. Once the settings and schedule have been finalized we recommend that the devices is set up at home and tested for at least a week to determine proper functionality of both the hardware and web interface. This can be accomplished from call playbacks and testing to see if the calls are rerported on the Instinct Environmental web portal.&#x20;

### Recommended Setup & Schedule

Throughout this document we will reference our recommended schedule setup. This schedule is defined as follows:

* 2hrs on, 1 hour off, from 4pm - 6am
* \[4pm–6pm], \[7pm–9pm], \[10pm–12am], \[1am–3am], \[4–6am]
* Expected notifications received: 6:28pm, 9:28pm, 12:28am, 3:28am, 6:28am.
* Total recording time: 10 hours
* Sample Rate: 48 kHz - BirdNET recommended Setup
* Number of channels: 1 (mono) - BirdNET compatible
* Expected days to full storage - assuming 1TB memory upgrade: 296
* Assume solar is connected, receiving full sun - partial shade.

{% file src=".gitbook/assets/recommended_schedule.txt" %}

Given this setup we can assume the device will be able to run for 290+ days without maintenance - more than enough to be deployed for the entirety of the bullfrog calling season.&#x20;

### Looking Forward

The ASU 2 promises to be an effective system for generating near real time alerts for bullfrog activity - allowing eradication teams to respond quickly to any new detections. This rapid response is necessary in sensitive habitats due to the speed at which an introduced bullfrog can begin reproducing - at which point eradication efforts become much more difficult and costly.

Deployment of ASU2 for an entire field season will put them through a more rigorous testing under field conditions such as extreme heat, sunlight, and other stressors that were not replicated during our testing. However, the ASU2 has been deployed in the field by spotted owl biologists in the Pacificn NorthWest of North America and is expected to perform well. One variable that we did not test is the sensitivity of the speaker to real world bullfrog calls under typical field conditions. Understanding this requirement will help determine how far from the high water mark the devices should be deployed as well as how many are needed for complete coverage of an area.&#x20;

Please also note that the ASU2 is not waterproof, care should be taken to avoid the possibility of accidental inundation during storm events when water levels can increase rapidly.&#x20;





