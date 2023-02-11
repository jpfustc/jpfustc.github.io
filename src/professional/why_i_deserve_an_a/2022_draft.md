
<!--
## January to February: 

High accuracy interpolation

**Requirement**

* meet customer accuracy demand

**Contribution**

* Beat previous method by a big margin (<1/20 versus 1/10)
* Interpolation solution for SVA
* Thorough analysis of the problem (window type/para, SNR, offset, high speed signal distortion)
    * Mathematical analysis, instead of try and fail

**By products**

* Thorough study of radar test system
    * Doppler implementation; Doppler frequency computation (carrier frequency and speed of light); Phase distortion issue
    * The results was summarized and delivered to solution team as they evaluate next radar test system purchase
* Thorough study of high speed effect
    * Signal smear (range migration)
    * range and Doppler drift
* Bugs in Alps firmware high speed compensation

**Problems**

* 202203
* Perhaps 3 weeks wasted on bitwidth optimization
    * Preserve sufficient bits at each stage to contain quantizationn error while minimizing bitwidth
    * 64 LUT & 7 bit fixed point division turn out to be cheap for RTL. Just adopt a sufficient bitwidth
    * Such principle does apply to front end, where memory saving is more important
    * TODO review Ricky's plan for FFT
    * PJ: classic example of pre mature example

* 202208
* Perhaps another 3 weeks on accurate math regression
    * Experiments fits perfectly with simulation
    * Perhaps such over effort was not necessary
    * PJ: mathematical statistics, analysis of variance. Measure effectiveness could be simpler than math proof

**Risks**

* Limited value in real scenario
    * Sparse signal assumption
    * Lack of measurement of effectiveness in roadtest scenario

* SVA mainlobe shape variance
    * Argument with Qiyong

* DA: unable to perform range accuracy interpolation
    * Architecture issue
    * 202208: more input from Ricky: tap filter of 3 range gates

**Lessons**

* Angle interpolation
    * Zhu, yan was the only persons insisting on having angle interpolation
    * 5 bits versus 4 bits?
    * We later pointed to the problem of redundant dense steering vector
    * The product design decision was still questionable

* Project management
    * PRS was never mentioned over the entire project span

## March DDM analysis

**Problem**

* Abnormal and non-linear DDM sidelobe level with multi TXs simultaneously activated

**Contribution**

* Proof non-linearity and propose cross channel coupling model with coprime DDM cycle experiment

## Feb/Aug Conti RFQ algorithm analysis

**Problems**

* Conti provided two set of sample codes as part of RFQ.

**Contributions**

* Crack the actual applications behind the samples codes: Conti DA CFAR/Conti OMP SAR, perhaps for OMP

## April to May Pro Firmware and FPGA validation

**Contribution**

* Develop FW bottom level driver for all HWA engines
* Bitmach of 5/7 validation cases on FPGA; driver debugging

## June to September Andes M0 validation

**Contribution**

* Develop validation plan from scratch
* Maximized coverage
* Continuous support for digital and FW debugging. 30 issues documented so far, average repsonse time of one day.

## July MBC study

## August to October Andes A0 validation

****
--!>
