# Bullfrog ASU2 Report

## Summary

We evaluated the effectiveness of Instinct Environmental's Acoustic Surveying Unit 2 (ASU2) for American bullfrog (Rana catesbeiana; RACA) detection. The ASU2 was deployed with an open source BirdNET(V2.0.0) acoustic detection model onboard. As the name implies, the BirdNET model is focused on birds but also includes a handful of frogs, including RACA. With the BirdNET model onboard, the ASU2 hardware provides a timely analysis of recorded audio data to identify species. After the ASU2 analyzes the audio any positive identifications are relayed to a satellite and uploaded to Instinct Environmental’s web portal. The purpose of this project was to evaluate ASU2 hardware functionality for RACA detection under field conditions. The insights and lessons learned from this evaluation will guide future deployments of the ASU2 (or similar) hardware by The Nature Conservancy and their partners.&#x20;

This evaluation of the ASU2 was focused on hardware reliability, power consumption, satellite transmission reliability, and recording schedule guidelines. Note that an evaluation of the BirdNET model is outside of the scope of this work and would be redundant in nature. Peer reviewed research by Bota et al. (2024) demonstrated that the BirdNET model is highly effective for RACA detection.&#x20;

The overall result demonstrates reliable transmission of positive RACA detections from the ASU2 in a field environment (note that the field detections in this work came from audio playbacks in urban environments). When using the recommended recording schedule and settings, and paired with a solar panel/battery, the ASU2 is expected to run for approximately 290 days without interruption. Because RACA are relatively sedentary during the winter months, a breeding season deployment of ASU2 from March to November each year can readily detect calling activity during the peak breeding season, with an extensive temporal buffer. Automated transmission of species identification results from the ASU2 greatly reduce the need for field staff hours, while providing near real-time information on the presence of invasive RACA. This tool creates critical early detection and rapid response opportunities to address recolonizations of invasive RACA in sensitive habitats.

Automated transmission of species identification results from the ASU2 greatly reduce the need for field work by eliminating regular memory card retrievals and remove the need to analyze audio data on local workstations. The near real-time information on invasive RACA presence, allows monitoring programs to adopt an early detection and rapid response paradigm to quickly stop new infestations before they spread. Labor hours that would have previously focused on monitoring can now be shifted towards control activities.&#x20;

## Overview

During field testing, the ASU2 demonstrated a high level of reliability and is projected to provide near real-time audio monitoring in the field for nine months (296 days) without maintenance using the recommended recording schedule (see Recommended Schedule section below). The nine month limit occurs when the usb storage drive reaches capacity. A data file of each audio recording is stored on the usb drive after it is analyzed and all audio recordings are saved, regardless of positive detection or not. Storage of audio recordings allow for a later manual review when the USB drive is physically removed from the ASU2 hardware and the data is downloaded to a computer. This is useful when verification of a positive detection is needed due to a rare or unexpected detection reported by the ASU2.  Of course, if there is a need to extend the duration of recordings beyond nine months, the recording schedule can be adjusted to record less often, extending the timeline until the usb drive reaches capacity. Note that the audio recordings are not transmitted remotely to the web portal over satellite, only the detection results are sent.

(Please note that all field testing was conducted in an outdoor urban environment with call playbacks from recordings because we missed the RACA calling season).

During field testing, the ASU2 demonstrated excellent reliability with all RACA call playback bouts detected by the onboard hardware and successfully relayed to the satellite and the Instinct Environmental web portal. The ASU2 is projected to provide near real-time audio monitoring for nine months (296 days) without maintenance using the recommended schedule, detailed in the following section. The nine month limitation arises from the USB storage filling up. A data file of each audio recording is stored on the USB drive after it is analyzed and all files are saved, regardless of a positive detection or not. In case there is a need to review a specific audio file it can be retrieved manually by physically uploading the data from the usb drive. Note that the audio files themselves cannot be transmitted remotely to the web portal over satellite, only the detection results can be sent. Of course, if there is a need to extend the duration of recordings beyond nine months, a less frequent recording schedule will extend the time before the usb drive reaches capacity. <br>

Powering the ASU2 with the optional solar module and the standard battery promise to provide power for a hypothetically indefinite amount of time. In this case the device can operate continuously with field visits being limited to the need to download or swap out the USB drive and perform solar panel maintenance.

The device is capable of uploading results to the web portal within thirty minutes of a scheduled recording bout finishing. The timely reporting framework of the ASU2 allows for rapid response to  RACA presence within sensitive habitats. As previously stated, our testing consisted of RACA audio playbacks in outdoor urban settings. We tested multiple recording schedules and determined that at least 30 minutes are needed between recording bouts so that the ASU2 can analyze and then transmit the results to the satellite for relay to the web portal servers. If recording bouts are too close together the device will get stuck, ending the ability to record or submit data. To be on the safe side we recommend that one hour is used between bouts for all recording schedules.&#x20;

Audio playback bouts of RACA advertisement calls resulted in all bouts returning positive detections of bullfrogs. This result indicates that the BirdNET model is functional with the hardware and protocols of the ASU2 for accurate detection of RACA.

During our field tests we did discover important limitations which could result in additional field visits after the ASU2 is deployed. Schedule changes cannot be pushed remotely, and therefore any changes need to be manually uploaded via the USB drive. Additionally, changes to the BirdNet Algorithm settings need to be&#x20;

A key limitation of the ASU2 is the inability to be updated remotely - requiring a field visit to change settings such as the recording schedule or detection confidence threshold. This is accomplished by uploading the new schedule to the USB drive on the hardware.

### Recommended Setup & Schedule

Throughout this document we will reference our recommended setup and schedule, detailed below.&#x20;

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

