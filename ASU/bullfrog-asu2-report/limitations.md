# Limitations

The Following Limitations were observed for the ASU 2

* The devices cannot receive information remotely. This means to update/change anything about the configuration of the device requires accessing it in the field. For this reason it is important to plan ahead before deploying in the field. Actions that are required to be performed in the field for this reason include changes to any of the following:
  * Recording schedule
  * Minimum confidence threshold
  * Which algorithm is being used
  * Sample rate
  * Time zone
* Additional custom algorithms can only be updated by firmware updates. This requires shipping the devices to Instinct to perform the update. For the addition of our custom RADR model it also required a fee of $200. This also means that in the future if the BirdNET standard algorithm gets updated with new species or improved performance, it will require us to send the device back to Instinct for an update to receive that new functionality.
* Schedules cannot have a recording cross midnight. For example, you cannot record from 11:30pm-1am. This must be worked around.
* There is no way to tell how much battery the ASU has remaining remotely or in person.&#x20;
* Above 254 detections within a single recording slot, the device stops counting and only returns '254+ detections', potentially skewing results.
* The device can only run inference and send satellite transmission while not recording. This results in the following practical limitations:
  * No ability for constant monitoring - some amount of temporal loss is required.
  * Longer recording slots result in longer delays in notification.
* The device itself only has one led light as a status indicator. This makes it hard to tell what is actually happening if you need to debug in the field, as all indicator functions display as some form of the red light being on or blinking.
* The device is heavy, and could be difficult to deploy deep in the field.

We had some issues in the beginning of our work with Instinct that were related to them being a new company, and us being their first client using BirdNET on the ASU. During these instances Ashwin was quick to reply and provide solutions to the problems.

* The first device we deployed in the field fully malfunctioned. We were told “we took a quick preliminary look at the old ASU 4872609. It turns out, something was up with the circuit board, and power was not getting to the CPU! So some kind of defect.” Instinct shipped us a new device to replace the broken one, and provided extended satellite service to make up for lost time.&#x20;
* BirdNET detections did not display at all on the web interface at first, but were quickly added in.
* Similarly, the alert system (text, phone, email) did not work when we started our service, and were not created until a few months after we began.
