# FBG-Based Water-Level Detection System

**M.Tech Project | Instrumentation Technology | Department of Instrumentation, CUSAT**

This project investigates water-level detection using Fiber Bragg Grating (FBG) sensors. Two FBG sensors with distinct Bragg wavelengths were positioned at different heights in a water container. An optical interrogator was used to monitor wavelength changes while the water level was raised and lowered.

> **Scope note:** The water-level experiment was conducted and evaluated. Humidity sensing was explored as a proposed extension, but its experimental validation was not completed during this project phase. This repository documents the completed water-level work and identifies humidity sensing as future work only.

## Objectives

- Investigate the wavelength response of FBG sensors during rising and falling water-level conditions.
- Observe the response of sensors positioned at different heights.
- Calculate wavelength shifts from optical-interrogator measurements.
- Examine sensitivity, variation between trials, and temperature cross-sensitivity.

## Experimental Setup

Two FBG sensors were placed vertically inside a water container, with approximately 7 cm separation. The lower sensor was positioned near the bottom, and the second sensor was placed approximately 7 cm above it. Their distinct Bragg wavelengths enabled the responses to be distinguished by the optical interrogator.

![Experimental setup](images/experimental-setup.jpeg)

### Sensors used

| Parameter | Sensor 1 | Sensor 2 |
|---|---:|---:|
| Nominal Bragg wavelength | ~1545 nm | ~1550 nm |
| Measured wavelength range in reported trial | 1547.012–1547.059 nm | 1551.023–1551.072 nm |
| Wavelength shift in reported trial | 47 pm | 49 pm |

![FBG sensor 1](images/fbg-sensor-1545nm.jpeg)

![FBG sensor 2](images/fbg-sensor-1550nm.jpeg)

The sensors were separated vertically by approximately 7 cm. The report lists an FWHM of approximately 0.70 nm and a fiber length of approximately 10 m for the sensors.

## Measurement Procedure

1. Connect the FBG sensors to the optical interrogator.
2. Position the sensors vertically in the container at the specified separation.
3. Record the wavelength response while water is gradually added.
4. Continue recording as the water is gradually drained.
5. Calculate the wavelength shift for each sensor using:

   `Δλ = λ_max − λ_min`

6. Repeat the experiment to compare the measured shifts across datasets.

## Results

In the reported response trial:

- Sensor 1 changed from 1547.012 nm to 1547.059 nm, corresponding to approximately 47 pm.
- Sensor 2 changed from 1551.023 nm to 1551.072 nm, corresponding to approximately 49 pm.
- The report estimates an approximate sensitivity of 7 pm/cm using a 49 pm shift over a 7 cm separation. This is an approximate project-reported estimate, not a fully validated calibration over the complete level range.

### Wavelength response

The following plots are extracted from the project report.

![Sensor 1 wavelength response](images/sensor-1-wavelength-response.png)

![Sensor 2 wavelength response](images/sensor-2-wavelength-response.png)

### Variation across experimental datasets

| Dataset | Sensor 1 shift (pm) | Sensor 2 shift (pm) |
|---|---:|---:|
| 1 | 47.19 | 49.02 |
| 2 | 2.81 | 1.78 |
| 3 | 1.48 | 7.93 |
| 4 | 6.57 | 14.68 |
| 5 | 14.36 | 22.05 |
| 6 | 5.56 | 6.42 |

![Repeatability analysis](images/repeatability-analysis.jpeg)

The measurements varied noticeably between trials. The report identifies temperature variation, environmental conditions, handling, baseline drift and incomplete recovery as factors affecting repeatability. The system therefore demonstrated a measurable response, but not consistent repeatability across all datasets.

## Working Principle

An FBG reflects a characteristic Bragg wavelength, described by:

`λB = 2 neff Λ`

where `neff` is the effective refractive index and `Λ` is the grating period. Changes in temperature or strain alter these properties and shift the reflected wavelength. In this experiment, the air-to-water transition changed the sensor's thermal environment; the observed wavelength response was interpreted primarily as temperature-related. The response should not be described as a direct, independently calibrated measurement of hydrostatic pressure.

## Limitations

- Temperature cross-sensitivity affects wavelength measurements.
- The observed shifts are small and in the picometer range.
- Wavelength shifts varied considerably across repeated datasets.
- Baseline drift and incomplete recovery were observed.
- Further controlled calibration and temperature compensation are required.
- The humidity-sensing experiment was not completed in this phase.

## Future Work

- Improve repeatability through controlled experimental conditions.
- Develop and validate temperature-compensation methods.
- Perform additional calibration across controlled water-level increments.
- Experimentally validate the proposed polymer-coated FBG humidity sensor.
- Evaluate the system for practical water-ingress monitoring applications.

## Tools and Equipment

- Fiber Bragg Grating (FBG) sensors
- Optical interrogator
- Optical fiber and connectors
- Water container and level measurement arrangement
- Interrogator software / in-house GUI for wavelength monitoring

## Project Documentation

The diagrams, sensor photographs and plots in `images/` are extracted from the project report. The full project report and presentation can be added separately if you choose to publish them.

---

**Project author:** Anjana Mahendran  
**Institution:** Cochin University of Science and Technology (CUSAT)  
**Department:** Department of Instrumentation
