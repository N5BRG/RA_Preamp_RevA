# RA_Preamp_RevA

Copyright (c) 2026 Robert S. Stricklin Jr

This hardware design is licensed under the CERN Open Hardware Licence Version 2 - Permissive (CERN-OHL-P-2.0).

You may obtain a copy of the license in the `LICENSE` file included with this repository.

## Overview

This design is a Radio Astronomy Preamplifier intended for operation at 1420 MHz, which is approximately the frequency of the neutral hydrogen spectral line produced by the hyperfine spin-flip transition of hydrogen atoms in space. This signal is commonly referred to as the **Hydrogen Line** or the **21-centimeter Hydrogen Line**.

The goal of this preamplifier is to provide the lowest practical noise figure while amplifying extremely low-level radio signals. Included in the design is a PIN diode switch that allows switching between the antenna input and an alternate path terminated with a precision 50-ohm reference resistor. This approach is similar to the Dicke switching technique developed by [Robert H. Dicke](https://en.wikipedia.org/wiki/Robert_H._Dicke) in the mid-1940s for microwave radiometry and receiver calibration.

For best performance, the preamplifier is powered from a low-noise 5-volt power supply (5.5 V maximum). The PIN diode switch is controlled by an external voltage of approximately 1.8 to 2.5 volts applied to the control input for the ON state (3.3 V maximum), and 0 V to -20 mV for the OFF state. The analog RF ground and the digital switching ground are separated to minimize the possibility of switching noise coupling into the RF signal path.

The total current required by the preamplifier is approximately 160 mA, although this value may vary somewhat with temperature and component tolerances. At 5 volts and 160 mA, the power dissipation is approximately 800 mW at 25°C, so good thermal management should be considered when mounting the preamplifier in an enclosure.

The PCB is designed to plug into a power and control PCB. However, because the power board is longer, it may be more practical to mount the boards side-by-side if the power board is used. To minimize noise, a low-noise linear voltage regulator is recommended.

A graph showing the noise figure versus frequency, along with the gain of the preamplifier, is included with the project files. These measurements were obtained using an HP 8970B Noise Figure Meter. The 1420 MHz noise figure is 0.46 dB and the gain is 40.11 dB.

## Amateur Radio Astronomy

This design was created to support the educational and scientific goals of the Society of Amateur Radio Astronomers (SARA). Additional information about SARA can be found at:

https://www.radio-astronomy.org/

Many of the ideas incorporated into this design were discussed during SARA's regular monthly Zoom meetings and educational activities.

If you enjoy physics, astronomy, radio astronomy, electronics, and scientific experimentation, please consider joining SARA and participating in its programs. SARA is an especially good opportunity for students and young people who are interested in science, engineering, and technology. Most participation is conducted online through video conference meetings.

## Acknowledgements

If you use KiCad, please consider making a donation to the project to help support the continuing development and distribution of this outstanding open-source electronic design software.
