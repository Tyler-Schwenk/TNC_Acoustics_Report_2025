# ASU Report

## Summary

We evaluated the effectiveness of Instinct Environmental's Acoustic Surveying Unit 2 (ASU2) for American bullfrog (Rana catesbeiana; RACA) detection. The ASU2 was deployed with an open source BirdNET(V2.0.0) acoustic detection model onboard. As the name implies, the BirdNET model is focused on birds but also includes a handful of frogs, including RACA. With the BirdNET model onboard, the ASU2 hardware provides a timely analysis of recorded audio data to identify species. After the ASU2 analyzes the audio any positive identifications are relayed to a satellite and uploaded to Instinct Environmental’s web portal. The purpose of this project was to evaluate ASU2 hardware functionality for RACA detection under field conditions. The insights and lessons learned from this evaluation will guide future deployments of the ASU2 (or similar) hardware by The Nature Conservancy and their partners.&#x20;

This evaluation of the ASU2 was focused on hardware reliability, power consumption, satellite transmission reliability, and recording schedule guidelines. Note that an evaluation of the BirdNET model is outside of the scope of this work and would be redundant in nature. Peer reviewed research by Bota et al. (2024) demonstrated that the model is highly effective for RACA detection.&#x20;

The overall results indicate that ASU2 reliably transmits positive detections of RACA in a field environment. Using our recommended recording schedule and settings, paired with a solar panel and battery, the ASU2 is expected to run for approximately 290 days without interruption. Because RACA are relatively sedentary during the winter months, a breeding season deployment of ASU2 from March to November each year can readily detect calling activity during the peak breeding season, with an extensive temporal buffer. Automated transmission of species identification results from the ASU2 greatly reduce the need for field staff hours, while providing near real-time information on the presence of invasive RACA. This tool creates critical early detection and rapid response opportunities to address recolonizations of invasive RACA in sensitive habitats.

## Overview

During field testing, the ASU2 demonstrated a high level of reliability and is projected to provide near real-time audio monitoring in the field for nine months (296 days) without maintenance using the recommended recording schedule (see Recommended Schedule section below). This limitation arises from the usb storage drive reaching capacity. A data file of each audio recording is stored on the usb drive after it is analyzed and all files are saved, regardless of a positive detection or not. In case there is a need to review a specific audio file it can be retrieved manually by physically uploading the data from the usb drive. Note that the audio files themselves cannot be transmitted remotely to the web portal over satellite, only the detection results can be sent.

Of course, if there is a need to extend the duration of recordings beyond nine months, a less frequent recording schedule will extend the time before the usb drive reaches capacity.&#x20;

<br>

Solar power combined with a substantial battery promise to provide power for a hypothetically indefinite amount of time.

The device is capable of uploading results within thirty minutes of a scheduled recording finishing - allowing rapid response to the presence of RACA within sensitive habitats.

While more testing in real world conditions are needed, the underlying BirdNET algorithm has been shown to be effective at identifying bullfrog vocalizations within audio files.

Some key limitations include the inability for the device to retrieve data/updates remotely - requiring a visit to the field to change settings such as the recording schedule or detection confidence threshold.

### Recommended Setup

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

The ASU 2 promises to be an effective system for generating real time alerts for bullfrog activity - allowing eradication teams to respond within a day of introduction to the site. This rapid response is necessary in sensitive habitats due to the speed at which an introduced bullfrog can begin reproducing - at which point eradication efforts become much more difficult and costly.

We recommend deploying the devices in the field to provide a better understanding of its capabilities under real world environmental variability. Field deployment would help determine detection accuracy metrics, and the best setup for the device & model when monitoring within our local acoustic domain. It would also provide confirmation of system reliability when exposed to direct sunlight, elevated temperatures, and other site-specific stressors that cannot be fully replicated in controlled testing.



