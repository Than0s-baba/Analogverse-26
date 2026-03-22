# Analogverse-26
Project created for the Analogverse competetion held during Ingenium 2026, the annual techno cultural fest of IIT Indore. 

> The signals going around in the brain are quite small but still detectable through the thick skull and the skin. using general electrode inputs from the scalp, we can harness these signals, however, there exists a lot of noise and disturbances in the surroundings that hamper strongly with our readings, to clear those off and get our brain signal readings ready for processing, we have this project. :shipit:

## [The Problem Statement](https://docs.google.com/document/d/1ZouESIPnIgMfJ_Vj_Cs22WRU7gU9RRMwYfacLmLEe94/edit?tab=t.0): 
The Alpha-Wave Brain Computer Interface Front-End
The human brain emits distinct electrical patterns based on mental states. Alpha waves (8 Hz to 12 Hz) are prominent when a person is relaxed with their eyes closed. However, these signals at the scalp are incredibly weak (10 µV to 50 µV) and are easily drowned out by the 50 Hz powerline interference radiating from every wall outlet, as well as baseline wander from patient movement.
The Task: Design a single-channel, wearable Analog Front-End (AFE) that isolates and amplifies Alpha brainwaves from raw scalp electrode inputs. The output must be a clean, amplified signal ready to be fed into an standard 3.3V ADC (like an ESP32 or Arduino) for relaxation detection.
### Design Specifications:
- Total System Gain: 1000 to 5000 V/V (distributed appropriately to prevent rail saturation).
- Frequency Response (Bandpass): Strictly pass the 8 Hz to 12 Hz Alpha band. Frequencies below 0.5 Hz (DC offset/sweat artifacts) and above 30 Hz (muscle noise/EMG) must be heavily attenuated.
- Noise Rejection: Must include a dedicated stage to aggressively reject 50 Hz mains hum (minimum -40 dB attenuation at 50 Hz).
- Input Stage: Must handle differential inputs from three electrodes (Active, Reference, and Right Leg Drive/Ground) with a very high Common-Mode Rejection Ratio (CMRR).
- Power Supply: The circuit must operate on a single-supply (e.g., 3.3V or 5V) or dual-supply (+/- 5V or +/- 9V) derived from batteries, fitting a wearable form factor.
- PCB Constraints: Maximum board size of 100mm x 100mm.

### Deliverables:
**Phase1**: Simulation Instructions are attached, the Phase 1 Submission should involve output of the test mentioned , along with a report on the designed circuit justifying component choice.
**Phase2**: The Spice models will be tested with instantaneous testbenches on the location , the detailed presentation with simulation results and PCB layout to be presented in front of the Judges.

## [The Solution to Phase 1](Phase1/report.pdf)

## The Solution to Phase 2
too much efforts for completing and documenting the second part alone so just sharing the file. basically creating the whole schematic of the Phase 1 onto a PCB
![image of pcb board in kicad](/Phase2/pcb.png)



