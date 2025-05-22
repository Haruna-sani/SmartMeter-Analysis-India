# Smart Meter Readings Analysis in India

## Overview

This repository presents an analysis of smart meter electricity consumption data from two Indian cities, Bareilly and Mathura. The study explores power consumption patterns across the top meters in each location, highlighting variability, demand differences, and forecasting performance using machine learning models.

---

## Observations

### Observation 1: Bareilly Meters Analysis
- The top five meters in Bareilly show distinct power consumption patterns.  
- Meter **BR06** stands out with the highest average consumption (~15.82 kWh), nearly double that of others, and exhibits significant variability (std dev = 5.66) with values ranging from 6.06 to 44.37 kWh. This suggests it serves a high-demand user, such as a commercial site or dense residential area.  
- Meter **BR28** records the lowest mean consumption (~6.54 kWh) with a narrow range, indicating lower or intermittent usage, likely from smaller households or limited operational hours.  
- Meters **BR11**, **BR15**, and **BR29** are mid-range consumers with moderate average usage. Notably, **BR15** shows occasional high usage days, reflected in a wide spread (1.78 to 34.14 kWh) and a standard deviation of 4.86.  
- Overall, BR06 shows intense and variable usage, while BR28 is more consistent and low, highlighting diverse energy demands in Bareilly.

### Observation 2: Mathura Meters Analysis
- Mathura's top meters show wider variation in consumption.  
- Meter **MH10** has the highest average consumption (~16.29 kWh) and the greatest variability (std dev = 13.01), ranging from very low (0.28 kWh) to very high peaks (59.77 kWh), indicating fluctuating power demand.  
- Meters **MH11** and **MH43** have similar means (~12.18 and 12.15 kWh) but MH43 shows more variability and skew in consumption patterns.  
- Meters **MH21** and **MH25** show moderate consumption (~9.8 and 9.66 kWh) with relatively lower minimum values and variability.  
- MH10 likely represents a high-demand user with significant fluctuation, while others are more consistent, useful for targeted energy management in Mathura.

### Observation 3: Comparative Insights
- Both **MH10 (Mathura)** and **BR06 (Bareilly)** have the highest demands in their regions but differ in consumption profiles.  
- MH10 exhibits wider, more volatile usage with extreme peaks and troughs, while BR06’s consumption is steadier and more predictable.  
- These differences may reflect regional factors such as user behavior, industrial activity, or infrastructure, influencing energy planning strategies—predictable forecasting for BR06, dynamic management for MH10.

---

## Model Performance Summary

| Meter | RMSE   | MAE    | R²      | Final Loss |
|-------|--------|--------|---------|------------|
| BR11  | 2.3778 | 1.4604 | 0.3590  | 0.011829   |
| BR15  | 2.8822 | 1.6031 | 0.6615  | 0.007416   |
| BR29  | 2.3689 | 1.5476 | 0.5749  | 0.014238   |
| BR06  | 5.3758 | 3.2523 | 0.2481  | 0.015416   |
| BR28  | 1.3131 | 0.8316 | 0.8083  | 0.008592   |
| MH11  | 1.9966 | 1.4412 | 0.9150  | 0.012555   |
| MH25  | 2.0147 | 1.4485 | 0.7906  | 0.007510   |
| MH43  | 1.8347 | 1.3138 | 0.9178  | 0.006317   |
| MH10  | 4.1807 | 2.7465 | 0.8946  | 0.007027   |
| MH21  | 2.4400 | 1.7783 | 0.8199  | 0.011461   |

The performance metrics indicate varied prediction accuracy across meters, with some showing strong fits (e.g., MH43, MH11) and others reflecting more challenging patterns (e.g., BR06, MH10).

---

## Conclusion

This analysis highlights significant diversity in power consumption across meters and locations in India. Understanding these patterns is crucial for improving load forecasting, demand management, and energy optimization strategies tailored to user-specific or regional behaviors.

---


