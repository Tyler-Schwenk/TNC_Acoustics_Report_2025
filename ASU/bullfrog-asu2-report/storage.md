# Storage

Storage usage was directly related to the amount of time recorded per day. Recording storage used was consistent for each file per schedule. The ASU 2 uses a 256 GB SanDisk mini USB storage stick. This can also be upgraded to 512GB \[\~45$] or 1TB \[\~90$]. Due to the large increase in capacity for its value - and the fact that storage will likely be the limiting factor for deployment length - we recommend upgrading to the 1 TB storage option.

The web app does report the amount of storage remaining on the device to the user.

### Given our Recommended Schedule

* Data per recording (120 min @ 48 kHz): 675 MB
* Data per day (5 recordings/day): 3.375 GB/day
* Days to full (1TB) - **296 Days**

***

### How adjustments affect storage use

All changes described below assume only one parameter is adjusted at a time, with all others held constant. Given parameters being considered individually, all factors scale storage usage linearly.

#### Recording Length

Increasing total daily recording time increases storage usage linearly and reduces the number of days until storage is full proportionally.

* **Doubling daily recording time** → **halves days to full**
* **Increasing daily recording time by 50%** → **reduces days to full by 33%**

Using the recommended configuration:

* **Current:** 10 hours/day → **\~296 days to full (1 TB)**
* **Increased:** 15 hours/day → **\~197 days to full (1 TB)**

#### Sample Rate

Relative to the 48 kHz baseline:

* **32 kHz → 0.67× storage**
* **16 kHz → 0.33× storage**

**All else the same;**

* 32 kHz → **2.25 GB/day**, **\~444 days to full**
* 16 kHz → **1.125 GB/day**, **\~889 days to full**

**Interpretation**

Sample rate has a large impact on long-term storage. Dropping from 48 kHz to 32 kHz increases storage lifetime by \~50%. However BirdNET runs inference at 48 kHz - meaning any recordings produced at lower frequencies will be upsampled before processing. This could result in reduced performance of the algorithm - a tradeoff that is currently not necessary given our lengthy storage capacity at 1 TB is more than enough for deployment for a season.

#### Storage Capacity

Direct relationship:

* 256 GB \~76 days to full
* 512 GB \~152 days&#x20;
* 1 TB (1000 GB) \~296 days

