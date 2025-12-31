# Solar

## Solar Power Estimate – 10W Panel (NPA10S-12I)

Instinct Environmental provides a[ Newpowa NPA10S-12I 10Watt](https://www.solarflexion.com/product-p/NPA10S-12I.htm?utm_source=google\&utm_medium=cpc\&utm_campaign=\&utm_term=\&gad_source=1) solar panel for use with the ASU. Given the specs of this solar panel, we can estimate the amount of power supplied by the panel under various setup and environmental conditions.

As a whole, we can expect the solar panel to supply enough power to keep the ASU 2 running even during the winter under partial shade.

***

## Overview

The amount of power supplied by the solar panel varies greatly due to factors such as its positioning, the time of year, local weather, debris on the panel, etc. With that in mind, we have the following estimates for expected power supplied by the panel:

| Condition                     | Assumptions         | Estimated Wh/day   |
| ----------------------------- | ------------------- | ------------------ |
| Winter - Full sun, ideal tilt | PSH 5.9, derate 0.8 | **≈ 47 Wh/day**    |
| Winter - Full sun, off-angle  | \~65-85% of ideal   | **≈ 30–40 Wh/day** |
| Winter - Heavier shade        | \~25% of ideal      | **≈ 12 Wh/day**    |
| Spring - Full sun, ideal tilt | PSH 6.2, derate 0.8 | **≈ 50 Wh/day**    |
| Spring - Full sun, off-angle  | \~65-85% of ideal   | **≈ 33–45 Wh/day** |
| Spring - Heavier shade        | \~25% of ideal      | **≈ 13 Wh/day**    |

Given our average energy use from the ASU 2 at \~24 WH/day - combined with a very large battery bank at 1280 Wh, **we can expect the ASU 2 to be able to power itself unattended in the field for a full year or longer**, even under less than ideal conditions.

***

### Panel Specs

From the datasheet:

* **Model:** NPA10S-12I
* **Rated Power (Pmax):** 10 W @ STC
* **Vmp / Imp:** 17.37 V / 0.69 A
* **Voc / Isc:** 20.04 V / 0.73 A
* **Cell Type:** Monocrystalline, \~21.3% module efficiency

At STC (ideal lab conditions), the panel can produce **10 W** at peak sun. Daily energy output depends on:

* How many peak sun hours the panel gets
* Mounting angle and orientation
* Losses (temperature, dirt, shading, etc.)

***

### Solar Resource in San Diego

San Diego has a strong solar resource:

* Annual average solar radiation ≈ **6.1 kWh/m²/day**
* Fixed-tilt peak sun hours ≈ **5.7 hours/day** on average

Using monthly data for San Diego

* **Jan:** 5.63 kWh/m²/day
* **Feb:** 5.68 kWh/m²/day
* **Mar:** 6.29 kWh/m²/day
* **Apr:** 6.24 kWh/m²/day
* **May:** 6.24 kWh/m²/day
* **Jun:** 6.11 kWh/m²/day

For this document we’ll use:

* **Winter (Jan–Mar) average PSH:** ≈ **5.9 h/day**
* **Spring (Apr–Jun) average PSH:** ≈ **6.2 h/day**

(“Peak sun hours” here is effectively **kWh/m²/day ≈ equivalent full-sun hours**.)

***

### Method & Assumptions

We estimate daily energy as:

$$
\text{Wh/day} \approx P_{\text{rated}} \times \text{PSH} \times \text{system\_derate}
$$

Where:

* **P\_rated:** 10 W
* **PSH:** seasonal peak sun hours (winter vs spring)
* **System derate:** real-world efficiency factor

We’ll use these derate factors:

* **Ideal full sun, good tilt, clean panel:** **0.8**
* **Realistic average full sun:** **0.7**
* **Suboptimal tilt / mild issues:** **0.6**
* **Partial shade (branches, nearby obstructions):**
  * **Moderate shade:** multiply full-sun energy by **0.5**
  * **Heavier shade:** multiply full-sun energy by **0.3**&#x20;

Tilt assumptions:

* **“Near-ideal tilt”:** fixed, facing south, tilt \~20–30° (good for San Diego)
* **“Off-angle”:** up to \~15–20° off from ideal or slightly wrong azimuth (e.g. SE or SW instead of due south), typically costing \~10–15% energy.

***

### Winter (January–March)

**Average PSH:** \~5.9 h/day

#### 1. Full Sun – Near-Ideal Tilt

* Theoretical max:\
  10 W × 5.9 h ≈ **59 Wh/day**
* **Upper bound (derate 0.8):**\
  59 × 0.8 ≈ **47 Wh/day**
* **Realistic average (derate 0.7):**\
  59 × 0.7 ≈ **41 Wh/day**
* **Conservative lower bound (derate 0.6):**\
  59 × 0.6 ≈ **35 Wh/day**

#### 2. Full Sun – Off-Angle / Slightly Suboptimal

Assume \~10–15% loss relative to near-ideal tilt:

* **Average:** \~41 Wh/day × 0.85 ≈ **35 Wh/day**
* Practical range: **30–40 Wh/day**

#### 3. Partial Shade

Treat as a fraction of the full-sun energy:

* **Moderate shade (\~50% of full sun):**
  * Average: \~41 Wh/day × 0.5 ≈ **20 Wh/day**
* **Heavier shade (\~30% of full sun):**
  * Average: \~41 Wh/day × 0.3 ≈ **12 Wh/day**

***

### Spring (April–June)

**Average PSH:** \~6.2 h/day

#### 1. Full Sun – Near-Ideal Tilt

* Theoretical max:\
  10 W × 6.2 h ≈ **62 Wh/day**
* **Upper bound (derate 0.8):**\
  62 × 0.8 ≈ **50 Wh/day**
* **Realistic average (derate 0.7):**\
  62 × 0.7 ≈ **43 Wh/day**
* **Conservative lower bound (derate 0.6):**\
  62 × 0.6 ≈ **37 Wh/day**

#### 2. Full Sun – Off-Angle / Slightly Suboptimal

Again assume \~10–15% loss:

* **Average:** \~43 Wh/day × 0.85 ≈ **37 Wh/day**
* Practical range: **33–45 Wh/day**

#### 3. Partial Shade

* **Moderate shade (\~50% of full sun):**\
  \~43 Wh/day × 0.5 ≈ **22 Wh/day**
* **Heavier shade (\~30% of full sun):**\
  \~43 Wh/day × 0.3 ≈ **13 Wh/day**

***

### Summary Tables

#### Winter – Expected Energy from 10W Panel (San Diego)

| Condition                   | Assumptions                        | Estimated Wh/day   |
| --------------------------- | ---------------------------------- | ------------------ |
| Full sun, ideal tilt        | PSH 5.9, derate 0.8                | **≈ 47 Wh/day**    |
| Full sun, realistic average | PSH 5.9, derate 0.7                | **≈ 41 Wh/day**    |
| Full sun, off-angle         | \~10–15% loss vs realistic         | **≈ 30–40 Wh/day** |
| Partial shade (moderate)    | \~50% of realistic full-sun output | **≈ 20 Wh/day**    |
| Partial shade (heavier)     | \~30% of realistic full-sun output | **≈ 12 Wh/day**    |

#### Spring – Expected Energy from 10W Panel (San Diego)

| Condition                   | Assumptions                        | Estimated Wh/day   |
| --------------------------- | ---------------------------------- | ------------------ |
| Full sun, ideal tilt        | PSH 6.2, derate 0.8                | **≈ 50 Wh/day**    |
| Full sun, realistic average | PSH 6.2, derate 0.7                | **≈ 43 Wh/day**    |
| Full sun, off-angle         | \~10–15% loss vs realistic         | **≈ 33–45 Wh/day** |
| Partial shade (moderate)    | \~50% of realistic full-sun output | **≈ 22 Wh/day**    |
| Partial shade (heavier)     | \~30% of realistic full-sun output | **≈ 13 Wh/day**    |
