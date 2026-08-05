## Structural Life Monitoring for Composite Gliders

### Methodology Report

**Revision Candidate 10 (RC10)**

*Based on: "Extension of Glider Life using Structural Life Monitoring" — J.L. Derouineau, FFVP / EGU* [7]

------

### 1. Purpose and Scope

This document describes the methodology used to assess and justify extended operational life for composite gliders using Structural Life Monitoring (SLM). The method calculates an Equivalent Fatigue Index (EFI) (§4.4) from onboard acceleration measurements and compares the measured operational severity against the accepted certification reference severity represented by the Kossira & Reinke Utility reference spectrum.

The purpose is not to determine the absolute physical damage state of the composite structure. The purpose is to apply the same conservative fatigue-severity calculation to both the certification reference spectrum and the measured operational spectrum. As long as cumulative EFI remains below the certification reference limit, and the required inspection and continued-airworthiness provisions are satisfied, continued operation beyond the certified Service Life Limit may be justified without modifying Type Certificate documents or certified structural limits.

The methodology is applicable only to composite gliders operated within the EASA CS-22 Utility-category flight envelope (some glider models considered for SLM were initially certified under the National Authority of the TC holder, but all Type Certificate Data Sheets are now listed under the EASA product list), for which a Service Life Limit has been established.  The method uses the Kossira & Reinke Utility reference load spectrum, recognized by EASA [8] (ABB.164). Aerobatic-category operation and any operation outside Utility-category limitations are excluded from the initial scope of SLM implementation.

------

### 2. Regulatory Basis

The method is consistent with the following regulatory framework:

- **CS 22.627** (Fatigue Strength): requires structures to be designed to avoid stress concentrations in normal service; does not explicitly mandate a specific life limit.
- **EASA CM-S-006**: endorses the use of Kossira & Reinke load spectra for fatigue analysis and testing of sailplanes.
- **CS-STAN / Part ML**: governs installation of onboard recorders and maintenance requirements.

EASA has already accepted multiple means of compliance for CS 22.627, including full-scale fatigue testing and static overload testing. SLM is proposed as an additional means of compliance for ageing glider life management. Similar measured-usage principles have been used in aviation usage monitoring and Individual Aircraft Tracking, particularly in military aviation. SLM does not attempt to reproduce those military approaches directly or claim that they are directly transferable to gliders; the relevant precedent is the general principle that measured usage can be compared with a conservative reference usage assumption, provided the method is controlled, conservative, and supported by inspections.

------

### 3. Key Principles

**Service Life Limit and Certification EFI Limit**

The certified Service Life Limit (typically 12,000 flight hours) corresponds to an accepted fatigue exposure established during type certification. Certification is demonstrated against the safety-factored life: with a Safety Factor of 3, structural integrity is shown for 36,000 hours of equivalent fatigue exposure. In classical Palmgren-Miner notation, the cumulative value is often denoted $D$, for damage, and $D=1$ is associated with the theoretical failure threshold. In this SLM methodology, the same mathematical quantity is denoted Equivalent Fatigue Index, or $EFI$, because it is used as a conservative usage-severity index rather than as a direct measurement of physical composite damage.

The reference condition for the SLM calculation is therefore:

$$
EFI_{ref,36000}=1
$$

for the safety-factored 36,000-hour reference exposure, and:

$$
EFI_{ref,12000}=\frac{1}{3}
$$

for the certified 12,000-hour service life. The certification EFI limit used by the SLM method is:

$$
\boxed{EFI_{limit} = \frac{1}{3}}
$$

This does not mean that the actual composite structure is assumed to fail at 36,000 hours, nor that its physical damage state is known at 12,000 hours. For SLM, the accepted certification reference exposure is deliberately treated as the full allowable fatigue-exposure budget. This is conservative because the method does not take credit for any unobserved residual margin beyond the certified exposure.

**SLM as a reference-spectrum comparison method**

SLM is not certification by analysis and does not replace the structural substantiation performed during Type Certification. It does not attempt to determine the absolute fatigue life of a composite structure, identify the critical structural location, or predict the critical composite failure mode.

The method has a more limited objective: it uses the already accepted certified life exposure as a conservative reference and compares it with the measured operational exposure of an individual glider. The Palmgren-Miner calculation is therefore used as an Equivalent Fatigue Index, calculated consistently for the reference spectrum and for the measured spectrum.

**Proportionality between load factor and structural stress**

Within the Utility-category certified flight envelope — defined by speed, configuration (flaps, airbrakes), and authorized mass loading — load-factor variations are used as the practical measured proxy for the stress variations used in the EFI comparison. This proxy is justified by the proportionality, during aerodynamic flight, between vertical load factor and the bending-related structural stress variations that drive the reference Kossira & Reinke fatigue spectra. The manufacturer's design ensures that no critical stress exceeds the allowable value for any authorized combination of these parameters.

This proportionality is applicable during aerodynamic flight phases. It does not hold during non-aerodynamic phases such as takeoff roll, landing roll, or winch launch. These phases shall therefore be excluded from the measured aerodynamic spectrum. The Kossira & Reinke spectra-generation and EFI-rate calculation uses only valid aerodynamic recording time. Any separate operational accounting for non-instrumented, invalid, or excluded time is controlled by the approved ICA, IOMM, or operational procedure.

The Palmgren-Miner calculation is applied to stress amplitudes associated with load cycles, not to absolute static stress values alone. For a given critical location, if the stress amplitude is proportional to the load-factor amplitude within the authorized Utility-category flight envelope, the unknown proportionality coefficient is absorbed into the calibration of the EFI model and cancels when the reference and real spectra are compared using the same method. The absolute value of this coefficient is therefore not required for the proposed EFI-ratio approach. This does not mean that all structural locations have the same stress for a given load factor or share the same proportionality coefficient; it means that, within the authorized Utility envelope and for aerodynamic flight phases, load-factor variations provide a consistent proportional basis for the reference-versus-measured fatigue-severity comparison.

**High Cycle Fatigue regime**

Glider structures are designed so that operational stress levels remain well within the elastic domain of materials. The structure is therefore considered to operate in the High Cycle Fatigue (HCF) regime, which justifies the use of a Basquin-type S/N curve representation for the conservative EFI calculation used in this methodology.

------

### 4. Methodology

#### 4.1 Reference Load Spectrum

The reference load spectrum for this methodology is the Kossira & Reinke Utility spectrum [2][8] (ABB.164). This is a deliberate initial-scope limitation: SLM is proposed at this stage only for gliders operated within Utility-category limitations. Aerobatic-category operation and any operation outside the Utility envelope are not credited under this methodology. The Utility spectrum is recognized by EASA (CM-S-006) as a basis for sailplane fatigue analysis. It is intentionally conservative: it covers the envelope of possible Utility-category glider usages and has built-in conservatism relative to typical operations.

The original Kossira & Reinke spectrum is published normalized to 6,000 flight hours. Because the certification EFI limit is anchored at the 12,000-hour life (§3), the published occurrences are scaled to the required exposure time before use in the EFI calculation. The original  Kossira & Reinke spectrum is used rather than the more recent KoSMOS variant: KoSMOS omits low load factor variations to shorten ground-test duration, but those omissions are not appropriate when the reference spectrum is being compared cycle-for-cycle against a real measured spectrum.

#### 4.1.1 Use of the reference spectrum in the methodology

The Kossira & Reinke Utility reference spectrum is used whenever EFI must be assessed against the certified reference basis. The detailed equations are introduced at the point where they are needed in the calculation:

1. The reference spectrum is scaled to the certified 12,000-hour life to anchor the EFI model to the certification EFI limit (§4.4).
2. Periods or phases without valid SLM data, including non-flight phases, are not included in the measured aerodynamic spectrum. Any separate operational accounting for these periods is controlled by the approved ICA, IOMM, or operational procedure.
3. For life-extension projection, the EFI produced by the reference spectrum is compared with the EFI produced by real flights over the same real-flight duration. Because this duration may be much smaller than the duration of the published reference spectrum, the lower integer part of the scaled reference occurrences is used to keep the comparison fair and conservative (§4.5).

#### 4.2 Real Load Spectrum Acquisition

The vertical load factor $N_z$ is recorded continuously during flight using a tri-axial accelerometer located as close as possible to the Center of Gravity, in a rigid area near the wing spar. Proximity to the CG minimizes contamination from centripetal accelerations during attitude changes, while a rigid mounting area avoids local structural flexibility corrupting the measurement. Atmospheric turbulence and trajectory induce load variations at relatively low frequency, typically below 10 Hz  (CS 22.341).

Accelerometer requirements:

- Minimum sampling rate: 20 Hz
- 6-face calibration at each annual inspection to ensure recorder performance
- Installation calibration with the glider in level-flight attitude and wings level, so that the recorder-corrected vertical axis is aligned with the gravity vector in the reference flight attitude

Data is stored on onboard electronic memory and uploaded to a central repository.

**Non-flight phases.** During takeoff roll, landing roll, winch launch, and any other phase dominated by non-aerodynamic forces, the proportionality between vertical load factor and structural stress no longer holds. The accelerometer signal from these sequences shall therefore not be used to build the real aerodynamic load spectrum. The Kossira & Reinke spectra-generation and EFI-rate calculation uses only valid aerodynamic recording time. Any separate operational accounting for excluded, invalid, or non-instrumented time shall be defined in the approved ICA, IOMM, or operational procedure.

#### 4.3 Load Spectrum Processing — Kossira & Reinke Counting Method

Both the reference and real spectra shall be processed using the same Kossira & Reinke counting method [2][8], ensuring a consistent and legitimate comparison. The purpose of this section is to define the controlled software algorithm used to transform valid aerodynamic load-factor data into the occurrence spectrum used by the EFI calculation.

The processing chain shall be:

1. Validate and select the aerodynamic flight samples to be credited by SLM.
2. Convert each valid load-factor sample into a 1024-class representation.
3. Apply the Kossira & Reinke hysteresis filter in 1024-class space.
4. Convert the retained filtered values into 32-class load-factor values.
5. Remove repeated consecutive 32-class values.
6. Extract the alternating peak/valley sequence.
7. Build the 32×32 raw Markov transition matrix.
8. Determine the average load factor for the processed sequence.
9. Transform the raw Markov matrix into upper and lower exceedance occurrences around the average load factor.
10. Produce the 32-class occurrence spectrum.
11. Compute the EFI and associated reporting quantities using §4.4 and Appendix B.

For real measured data, the same class mapping, filtering rule, peak/valley rule, Markov-matrix convention, average-load-factor convention, and exceedance transformation shall be used whenever raw samples are processed into an occurrence spectrum. The Kossira & Reinke Utility reference spectrum used for EFI shall enter the operational calculation directly as an approved machine-readable occurrence table derived from ABB.164. The EFI calculation shall apply the same load-factor class table and EFI equations to the approved reference occurrence table and to the real measured occurrence table generated by the software. The detailed software requirements for the Kossira & Reinke processing chain are defined in Appendix A. The detailed software requirements for EFI calculation and reporting are defined in Appendix B.

#### 4.4 Equivalent Fatigue Index — Palmgren-Miner Rule

The Palmgren-Miner rule provides a linear cumulative index for fatigue. In classical notation this value is often denoted $D$, for damage. In the present SLM method, the same mathematical quantity is referred to as the **Equivalent Fatigue Index**, noted $EFI$, to avoid implying that the calculation represents measured physical damage in the composite structure:

$$
EFI = \sum_i \frac{n_i}{N_i}
$$

where $n_i$ is the number of cycles at load factor level $i$, and $N_i$ is the number of cycles to failure at that level.

For SLM, the Palmgren-Miner rule is used primarily as a consistent comparison framework between two spectra: the reference spectrum and the measured real-flight spectrum. The absolute value of EFI should not be interpreted as a direct measurement of physical composite damage at a specific structural location.

$N_i$ values are derived from the reference spectrum and conservative fatigue parameters using the Basquin model. To simplify the notation, the positive EFI exponent is defined as:

$$
\boxed{k = -\frac{1}{b}}
$$

For the generic SLM methodology, the selected composite fatigue parameter is:

$$
\boxed{b=-0.16}
$$

and therefore:

$$
\boxed{k=6.25}
$$

The selected value is a conservative engineering parameter for ageing composite glider primary structures made predominantly from conventional GFRP/CFRP epoxy laminates. It is not intended to be a universal composite-material constant or a type-specific material property.

The value is selected from the supporting review of published fatigue-fit parameters for epoxy-based GFRP/CFRP composite structures. Wind-turbine blade composite data are used as the closest available published analogue because they involve large, lightly loaded GFRP/CFRP structures operating in high-cycle fatigue under variable-amplitude loading. In the SNL/MSU/DOE fatigue database review, the steepest identified epoxy GFRP stress-fit exponent among the retained primary comparison data is $B=b=-0.1556$ for a QQ1 glass/epoxy multidirectional laminate at $R=0.1$ [9]. Additional SNL/MSU/DOE epoxy GFRP data and AIAA/SNL-MSU-DOE database trends give less severe values, while carbon-dominated epoxy laminates show much shallower stress-life slopes [9][10]. General composite fatigue references also emphasize that fatigue parameters depend on material system, layup, stress ratio, manufacturing process, environment, defects, repairs, and failure mode [11][12][13].

The generic value $b=-0.16$ is therefore chosen because it is slightly steeper than the steepest retained GFRP epoxy value and remains strongly conservative for CFRP-dominated epoxy structures. The selected value shall be treated as a conservative EFI severity-weighting parameter for the generic SLM methodology. For a type-specific certification program, it should be confirmed by the certification authority and, where required, by representative material, detail, repair, environmental, or structural evidence.

The $N_i$ expression, calibrated against the certification EFI limit, is:

$$
\boxed{%
N_i \;=\; C'\,\bigl|\mathrm{LF}_i-LF_{average,ref}\bigr|^{-k}
}
$$

where the calibrated constant $C'$ is:

$$
\boxed{%
C' \;=\; 3 \;\sum_j n_{j,ref,12000}\,\bigl|\mathrm{LF}_j - LF_{average,ref}\bigr|^k
}
$$

where the symbols are defined as follows:

- $i$ — index of the load factor level at which $N_i$ is being evaluated.
- $j$ — summation index running over all load factor levels of the reference spectrum. It is used inside the constant $C'$ to distinguish the summation over the whole spectrum from the single level $i$ at which $N_i$ is evaluated. The two indices range over the same set of load factor classes; different letters are used only to avoid confusion between the bound summation variable and the free index $i$.
- $n_{j,ref,12000}$ — number of cycles (occurrences) at load factor level $j$ in the reference Kossira & Reinke Utility spectrum, normalized to the certified life of 12,000 flight hours and processed with the counting method of §4.3.
- $\mathrm{LF}_j$ — load factor value of class $j$; $\mathrm{LF}_i$ — load factor value of class $i$.
- $LF_{average,ref}$ — average load factor defined by the approved reference data package in accordance with Appendix A.7.
- $LF_{average,real}$ — average load factor generated by the Kossira & Reinke processing of the real measured data in accordance with Appendix A.7.
- $b$ — Basquin S/N slope exponent; $b = -0.16$ for the selected generic composite case.
- $k=-1/b$ — positive EFI exponent used in the EFI summations; $k=6.25$ for the selected generic composite case.
- $C'$ — proportionality constant linking load factor amplitude to the number of cycles to failure. It is not a free parameter: it is fixed by calibrating the reference-spectrum EFI against the certification EFI limit $EFI_{ref,12000} = 1/3$.

Because the same calibrated constant $C'$, EFI exponent $k$, load-factor class definition, and Kossira & Reinke counting method are applied to both the reference and the real spectra, the absolute value of the load-factor-to-stress proportionality coefficient cancels in the EFI ratio and need not be known. The amplitude term is evaluated relative to the average load factor of the spectrum being assessed: $LF_{average,ref}$ for the reference spectrum and $LF_{average,real}$ for the real measured spectrum.

Real-flight EFI accumulation is then:

$$
\boxed{
EFI_{real}\;=\;\frac{1}{C'}\sum_i n_{i,real}\,\bigl|\mathrm{LF}_{i}-{LF_{average,real}}\bigr|^k
}
$$

The core calculation defined in this methodology computes $EFI_{real}$ for the valid aerodynamic recording duration included in the processed data set. It does not require missing, invalid, excluded, or non-instrumented duration as an input to the Kossira & Reinke spectrum-generation or EFI-rate calculation.

If a certified continued-airworthiness decision requires accounting for operation without valid SLM data, that accounting shall be defined in the approved ICA, IOMM, or operational procedure. Such accounting may use the reference Kossira & Reinke Utility EFI rate for periods that receive no measured-usage credit, but it is outside the core spectra-generation and EFI-rate calculation defined in Appendices A and B.

#### 4.5 Life Extension Assessment

The EFI ratio $R$ quantifies the life extension potential:

$$
\boxed{R = \frac{EFI_{ref}}{EFI_{real}}}
$$

where both values are computed over the same observed flight duration $t_{real}$. Here $EFI_{ref}$ is the reference-spectrum EFI normalized to $t_{real}$ — not the full-life value $EFI_{ref,12000} = 1/3$ of §3 and §4.4 — and $EFI_{real}$ is the measured EFI of §4.4 over the same $t_{real}$.

To evaluate $R$ in practice, the reference and real spectra must cover the same exposure time. The published reference spectrum (normalized to 6,000 flight hours) is scaled down to $t_{real}$, and the floor function $\lfloor \cdot \rfloor$ is applied to the scaled reference occurrences to add conservatism (the real observation period $t_{real}$ being much shorter than 6,000 hours). The operational expression, using the EFI exponent $k$, is:

$$
\boxed{R = \frac{\sum_i \left\lfloor \dfrac{n_{i,ref}\,t_{real}}{6000} \right\rfloor \,\bigl|\mathrm{LF}_i - LF_{average,ref}\bigr|^k}{\sum_i n_{i,real}\,\bigl|\mathrm{LF}_i - LF_{average,real}\bigr|^k}}
$$

where $n_{i,ref}$ and $n_{i,real}$ are the occurrences at load factor level $LF_i$ in the reference and real spectra respectively. This is the same computation as §4.4: substituting the $EFI_{ref}$ and $EFI_{real}$ expressions into $R = EFI_{ref}/EFI_{real}$, the constant $C'$ is identical for both spectra and cancels, leaving only the spectra and the EFI exponent $k$.

The estimated life extension beyond the certified limit is:

$$
\boxed{t_{extension} = (R - 1) \times t_{remaining\;ref}}
$$

where $t_{remaining\;ref}$ is the flight time remaining until the certified 12,000-hour limit is reached under reference spectrum assumptions.

As an illustration, preliminary analysis of approximately 35 hours of flight data on an instrumented Janus B yielded an EFI ratio of about 26 for the selected composite parameter $k=6.25$, corresponding to a potential life extension of several thousand hours for typical training and cross-country operations. In the supporting white paper [7], this illustrative case corresponds to approximately 7,500 hours of extension for an aircraft with about 300 hours remaining to the certified 12,000-hour limit. The same data evaluated with a metallic-part parameter $k=5$ yields an EFI ratio of about 12, which may be useful when assessing the adequacy of continuing inspection intervals for metallic fittings and attachments. These figures are illustrative of the method rather than certified results. 

Life extension is conditional on the assumption that future operations follow the same load pattern as those already observed. $R$ and $t_{extension}$ are therefore recalculated at each Airworthiness Review Certificate (ARC) renewal based on accumulated data. $R$ is highly sensitive to occasional high-load maneuvers: as an order of magnitude, a single 4g maneuver every two flight hours can reduce $R$ by more than an order of magnitude relative to gentle cross-country flying.

------

### 5. Applicability and Limitations

- Identical to all other methods for fatigue life identification, this method is valid only when the glider is operated within its certified Utility-category flight envelope (speed, configuration, mass distribution, load factor, etc.).

- Aerobatic-category operation and any operation outside Utility-category limitations are excluded from the initial scope of SLM implementation. 

- SLM is not certification by analysis, does not determine the absolute physical damage state of the composite structure and does not identify the critical structural location or critical failure mode.

- SLM does not reopen/change the Type Certificate structural substantiation, it uses the approved certification life exposure as the conservative reference limit.

- SLM compares measured operational severity against this accepted reference severity.

- The Palmgren-Miner calculation is used as a common comparison framework for both spectra.

- The Basquin parameter $b=-0.16$ is used as a conservative severity-weighting parameter, applied consistently to both the reference and measured spectra. It should not be considered a universal GFRP/CFRP epoxy composite-material property.

- Missing, invalid, excluded, or non-instrumented data are not included in the measured aerodynamic spectrum. Any operational accounting for such periods is controlled by the approved ICA, IOMM, or operational procedure.

- The method remains dependent on Instructions for Continued Airworthiness (ICA): sensor calibrations, data processing, inspections, especially for defects, repairs, bonds, metallic fittings, and unforeseen local deterioration.

  

------

### 6. Concept of Operation associated with methodology

This section provides the methodology-level Concept of Operation (CONOPS) summary. The detailed CONOPS, release-to-service conditions, abnormal-case handling, and practical procedures are controlled by the STC certification package, in particular the Certification Programme, the CRI or equivalent means-of-compliance agreement, the Instructions for Continued Airworthiness (ICA), and the Installation, Operating and Maintenance Manual (IOMM) for the SLM recorder and associated data process.

The operational implementation shall be defined in those approved documents. They cover practical installation, calibration, data acquisition, data validation, processing, maintenance, inspection, reporting, and airworthiness decision rules. In particular, after operation beyond the certified safe-life limit has started, SLM availability, valid recorder calibration, validated EFI status reports, and the required inspections become conditions for continued airworthiness, as defined in the ICA and associated STC documents.

**Phase 1 — Instrumentation and Data Collection** *(below the certified life limit)*  
The SLM recorder is installed in accordance with CS-STAN / Form 123. Installation calibration and annual 6-face calibration are recorded in the aircraft logbook. Flight data are uploaded to the controlled SLM repository and processed using the approved toolset. Any flight or phase occurring without valid SLM data, including sensor fault, data corruption, missed calibration, or non-flight phases excluded from accelerometer-based processing, receives no measured-usage credit and is substituted at the reference EFI rate for the corresponding duration or operational exposure, as defined in the approved ICA and data-processing procedure.

**Phase 2 — EFI Evaluation at the Certified Life Limit**  
When the aircraft reaches the certified life limit, a dedicated structural inspection is performed in accordance with the approved ICA. The inspection covers the composite structure and the overall aircraft condition, including incidents, repairs, bonds, metallic fittings, and other items defined in the ICA. Continued operation may be authorized only if the inspection does not identify unacceptable findings and the approved EFI assessment shows:

$$
EFI_{total}<\frac{1}{3}
$$

**Phase 3 — Operation Beyond the Certified Life Limit**  
Operation beyond the certified life limit is a continuation of Phase 1 monitoring with additional continued-airworthiness controls. A Go/No-Go decision is made at each ARC renewal or other approved review point using the validated SLM EFI status report. The Go criterion shall include both the current cumulative EFI and the projected EFI rate: $EFI_{total}$ must remain below $1/3$, and the projected EFI rate must show that the $EFI=1/3$ limit will not be reached before the next scheduled inspection or review. Recurring structural inspections continue at a maximum interval of 1,000 flight hours or 5 years, whichever occurs first. The process continues until the aircraft exhausts its remaining EFI potential or another approved continued-airworthiness limit is reached.

------

### 7. Approval and Deployment Pathway

This section gives only the methodology-level approval context. The detailed certification artifacts, document list, compliance responsibilities, EASA involvement, and approval schedule are controlled by the STC Certification Programme and associated Master Document List.

SLM deployment should be supported by an approved certification pathway, such as an EASA Supplemental Type Certificate (STC) or another approval route accepted by the competent authority. The Certification Programme defines the compliance approach for the STC, including the applicable aircraft, the approved operating domain, the proposed means of compliance, the required certification artifacts, and the EASA involvement for review or approval.

The certification package should include, as applicable:

- Certification Programme;
- Certification Review Item (CRI) or equivalent agreement on the proposed means of compliance;
- SLM Methodology Report (this document);
- Instructions for Continued Airworthiness (ICA);
- Installation, Operating and Maintenance Manual (IOMM) for the SLM recorder and associated data process;
- validation reports, Master Document List, Compliance Check List, and Master Compliance Report, as defined in the Certification Programme.

The Certification Programme shall remain the controlling document for the detailed approval artifacts. This methodology report defines the EFI calculation principles, assumptions, and limitations; the ICA and IOMM define the operational procedures, inspections, calibration, data handling, abnormal-case treatment, and release-to-service conditions.

------

### 8. Appendix A — Kossira & Reinke Processing Rules for Software Implementation

This appendix defines the deterministic rules required to implement the Kossira & Reinke counting method consistently for both reference and real spectra [2][8]. It is intended to be used as the software requirements baseline for acquisition processing, load-spectrum generation, and verification of the Kossira & Reinke processing chain.

#### A.1 Constants and notation

The load-factor range used for the generic SLM methodology shall be:

$$
LF_{min}=-4g
$$

$$
LF_{max}=+6g
$$

The number of fine acquisition classes shall be:

$$
N_{fine}=1024
$$

The number of coarse Kossira & Reinke spectrum classes shall be:

$$
N_{coarse}=32
$$

The fine class width shall be:

$$
\Delta LF_{fine}=\frac{LF_{max}-LF_{min}}{1024}
$$

The coarse class width shall be:

$$
\Delta LF_{coarse}=\frac{LF_{max}-LF_{min}}{32}
$$

The Kossira & Reinke hysteresis threshold shall be expressed in fine-class units:

$$
DX=10
$$

unless a different approved value is explicitly specified in the approved calculation package.

The implementation shall use zero-based class numbering:

- fine classes: $0 \ldots 1023$;
- coarse classes: $0 \ldots 31$.

#### A.2 Load factor to 1024-class conversion

For each valid load-factor sample $LF$, the corresponding 1024-class value shall be:

$$
q_{1024}=\mathrm{clip}\left(
\left\lfloor
\frac{LF-LF_{min}}{LF_{max}-LF_{min}} \times 1024
\right\rfloor,
0,
1023
\right)
$$

where $\mathrm{clip}(x,0,1023)$ limits the value to the valid range.

The load factor associated with a fine class may be represented by the class center:

$$
LF(q_{1024}) = LF_{min} + \left(q_{1024}+\frac{1}{2}\right)\Delta LF_{fine}
$$

The selected conversion rule shall be applied consistently to real-flight processing, verification data, and any inverse synthetic-data generation used for tool validation. The approved Kossira & Reinke reference occurrence table is normally imported as an occurrence spectrum rather than regenerated from raw data; its load-factor class definitions shall be consistent with this appendix.

#### A.3 Hysteresis filtering in 1024-class space

The Kossira & Reinke filter shall be applied before reduction to 32 classes.

The first valid sample shall be retained as the first filtered value.

For each subsequent sample $q_{1024}(n)$, the sample shall be retained only if:

$$
\left|q_{1024}(n)-q_{1024,last\_retained}\right| > DX
$$

where $q_{1024,last\_retained}$ is the last retained filtered value.

Samples for which:

$$
\left|q_{1024}(n)-q_{1024,last\_retained}\right| \le DX
$$

shall be rejected as low-amplitude variation/noise for Kossira & Reinke counting.

The retained filtered sequence shall be stored as an auditable intermediate output when detailed processing evidence is required.

#### A.4 Reduction from 1024 classes to 32 classes

Each retained 1024-class value shall be converted to a 32-class value using integer division:

$$
q_{32} = \left\lfloor \frac{q_{1024}}{32} \right\rfloor
$$

The associated class-center load factor shall be:

$$
LF(q_{32}) = LF_{min} + \left(q_{32}+\frac{1}{2}\right)\Delta LF_{coarse}
$$

Repeated consecutive 32-class values shall be removed before peak/valley extraction, because they do not define a transition between different load-factor classes.

#### A.5 Peak and valley extraction

The input to peak/valley extraction shall be the filtered 32-class sequence after removal of repeated consecutive values.

A value shall be retained as a peak or valley when the sign of the local trend changes.

For three consecutive retained 32-class values $a$, $b$, and $c$:

- $b$ is a peak if $b>a$ and $b>c$;
- $b$ is a valley if $b<a$ and $b<c$.

The first and last values of the filtered 32-class sequence shall be retained as sequence endpoints if they are required to define the first or last transition of the processed segment.

After repeated consecutive values have been removed, the trend-change rule produces an alternating peak/valley sequence by construction. Therefore a non-alternating peak/valley sequence is not an expected data condition; it indicates either a software defect or an undefined edge case in the implementation. The approved implementation shall define the endpoint and plateau handling rules deterministically, and the final stored peak/valley sequence shall not contain duplicate consecutive values.

If the processed segment contains fewer than two peak/valley values, no Markov transition shall be generated for that segment.

The peak/valley sequence shall be stored as an auditable intermediate output when detailed processing evidence is required.

#### A.6 Raw Markov transition matrix

The raw Markov transition matrix shall be a 32×32 integer matrix $M$.

The matrix convention shall be:

$$
M(i,j) = \text{number of transitions from class } j \text{ to class } i
$$

where:

- column $j$ is the “from” class;
- row $i$ is the “to” class.

For each consecutive pair in the peak/valley sequence:

$$
p_n \rightarrow p_{n+1}
$$

the matrix cell shall be incremented as follows:

$$
M(p_{n+1},p_n) = M(p_{n+1},p_n)+1
$$

Diagonal transitions $M(k,k)$ shall be zero because repeated consecutive 32-class values are removed before peak/valley extraction and because a transition from a class to itself is not a peak/valley transition.

The total number of Markov transitions shall satisfy:

$$
\sum_i\sum_j M(i,j) = N_{PV}-1
$$

where $N_{PV}$ is the number of values in the peak/valley sequence.

For a closed sequence, each class shall have equal arrivals and departures:

$$
\sum_j M(k,j) = \sum_i M(i,k)
$$

For an open sequence, the first class may have one additional departure and the last class may have one additional arrival. This imbalance shall be reported but shall not by itself invalidate the sequence.

#### A.7 Average load factor convention

A single average-load-factor value shall be associated with each spectrum data set and shall be used consistently for both:

1. splitting a raw Markov matrix into upper and lower exceedance branches, when a Markov matrix is transformed into an occurrence spectrum; and
2. computing the load-factor amplitude term in the EFI calculation.

The methodology shall therefore avoid defining a separate “counting average” and “EFI average” for the same data set.

For real measured data processed from raw load-factor samples, the default average shall be the arithmetic mean of the valid aerodynamic load-factor samples used for the processed flight or processed data set:

$$
LF_{average,real} = \frac{1}{N}\sum_{n=1}^{N} LF(n)
$$

The corresponding average 32-class index used to split the Markov matrix shall be:

$$
k_{avg,real}=\mathrm{clip}\left(
\left\lfloor
\frac{LF_{average,real}-LF_{min}}{LF_{max}-LF_{min}} \times 32
\right\rfloor,
0,
31
\right)
$$

For the approved Kossira & Reinke Utility reference spectrum, the original raw input time history is not available for SLM processing. The operational EFI calculation shall therefore use the approved Utility reference occurrence table directly. The approved calculation package shall provide the reference data needed by the EFI software, including:

1. the approved Utility reference occurrence table derived from ABB.164;
2. the load-factor class mapping;
3. the normalization duration of the reference occurrence table; and
4. the reference average load factor $LF_{average,ref}$ used for EFI.

If the reference average load factor is not explicitly available from the approved reference data package, it shall be defined by an approved deterministic convention before release of the calculation package. The selected convention shall be documented and applied consistently in the EFI calculation.

The published Utility Markov matrix of ABB.163 may be included as an optional verification artifact. Its purpose is to check the software implementation of Appendix A.8 by verifying that the digitized Markov matrix, when transformed using the approved split convention, reproduces the approved occurrence spectrum. ABB.163 shall not be required as an operational input to the EFI calculation.

#### A.8 Markov matrix transformation into exceedance occurrences

When a raw 32×32 Markov matrix is generated from real measured data, it shall be transformed into a 32-class occurrence spectrum by counting upward and downward exceedances relative to the applicable average class $k_{avg}$. The same transformation may also be applied to a digitized ABB.163 reference Markov matrix for verification of the Kossira & Reinke interpretation, but that verification path is separate from the operational EFI input path.

The matrix convention remains:

$$
M(i,j) = \text{number of transitions from class } j \text{ to class } i
$$

where $j$ is the starting, or “from”, class and $i$ is the ending, or “to”, class.

For classes at or above the average class, $k \ge k_{avg}$, the occurrence count shall be computed from transitions that start below the considered class and end at or above the considered class:

$$
j < k \quad \text{and} \quad i \ge k
$$

The occurrence count is therefore:

$$
O(k) = \sum_{i=k}^{31} \sum_{j=0}^{k-1} M(i,j)
$$

For classes below the average class, $k < k_{avg}$, the occurrence count shall be computed from transitions that start above the considered class and end at or below the considered class:

$$
j > k \quad \text{and} \quad i \le k
$$

The occurrence count is therefore:

$$
O(k) = \sum_{i=0}^{k} \sum_{j=k+1}^{31} M(i,j)
$$

With this default convention, the average class belongs to the upper branch. No additional zeroing, smoothing, or replacement of the average-class occurrence shall be performed. If the approved reference package uses a different convention for the average class, that convention shall be explicitly documented and applied consistently to real measured spectra.

The approved ABB.164 occurrence table, in machine-readable form, is the reference input to the EFI calculation. ABB.163 is used only when performing an optional verification of the Markov-to-occurrence transformation.

The occurrence spectrum $O(k)$ shall be stored as an auditable intermediate output when it is generated by the SLM software.

#### A.9 Required Kossira & Reinke processing outputs

The software shall be capable of producing, for each real measured processed flight or data set:

1. valid sample count and processed duration;
2. 1024-class filtered sequence;
3. 32-class filtered sequence;
4. peak/valley sequence;
5. raw 32×32 Markov transition matrix;
6. average load factor $LF_{average,real}$;
7. average 32-class index $k_{avg,real}$;
8. upper and lower exceedance occurrence branches;
9. final 32-class occurrence table;
10. processing warnings and validity flags.

For the approved Utility reference data package, the software shall identify the source and version of the approved reference occurrence table, the reference average load factor, the normalization duration, and the load-factor class definitions. If ABB.163 is used for optional Markov-transformation verification, the verification report shall identify the digitized matrix source, the split convention, and the comparison result against the approved occurrence table.

#### A.10 Kossira & Reinke processing verification checks

The software shall verify and report the following processing-consistency checks for real measured data processed from raw samples:

1. the sum of the raw Markov matrix equals the number of peak/valley transitions;
2. diagonal Markov cells are zero;
3. raw Markov row/column imbalance is consistent with the sequence start/end conditions;
4. the occurrence table was generated with the approved Kossira & Reinke algorithm version and parameter set.

A non-zero diagonal Markov cell shall be treated as a processing nonconformity.

If a digitized ABB.163 Markov matrix is used for optional verification, the software may use Appendix A.8 to check that the implemented transformation reproduces the approved Utility reference occurrence table. A discrepancy shall be treated as a verification issue to be resolved before relying on the transformation for real measured spectra.

#### A.11 Reference occurrence table

Implementation of the method requires the applicable Kossira & Reinke Utility reference occurrence table. That table shall be included in the approved calculation package in machine-readable form, together with the reference source, normalization duration, load-factor class definitions, reference average load factor, and any scaling convention used by the EFI calculation. 

------

### 9. Appendix B — EFI Calculation Rules for Software Implementation

This appendix defines the deterministic software rules used to compute EFI and associated life-extension quantities from the occurrence spectra generated by Appendix A.

#### B.1 Required inputs

The EFI software shall use the following inputs:

1. approved Kossira & Reinke Utility reference occurrence table, normalized to 6,000 flight hours;
2. real measured occurrence table generated by Appendix A;
3. valid real aerodynamic recording duration associated with the real measured occurrence table;
4. load-factor class-center table;
5. reference average load factor $LF_{average,ref}$, defined by the approved reference data package in accordance with Appendix A.7;
6. real average load factor $LF_{average,real}$, generated by the Kossira & Reinke processing of the real measured data in accordance with Appendix A.7;
7. Basquin exponent $b$;
8. positive EFI exponent $k=-1/b$.

For the generic SLM methodology:

$$
b=-0.16
$$

$$
k=6.25
$$

The 6,000-hour reference normalization, the 12,000-hour certified-life calibration basis, and the safety factor of 3 are fixed methodology rules, not free user inputs.

#### B.2 Average load factor used by EFI

The EFI calculation shall use the same average-load-factor value associated with each spectrum data set in Appendix A.7:

- $LF_{average,ref}$ for the approved Utility reference spectrum;
- $LF_{average,real}$ for the real measured spectrum.

The EFI calculation shall not compute a second independent average from the occurrence table unless that convention is explicitly approved as part of the reference calculation package. This avoids mixing a time-history or Markov-splitting average with an occurrence-weighted average, which could produce different numerical values.

#### B.3 Reference spectrum scaling

The published Kossira & Reinke Utility occurrence table is normalized to 6,000 flight hours.

For certification-limit calibration at 12,000 flight hours:

$$
n_{i,ref,12000}=2\,n_{i,ref,6000}
$$

For safety-factored reference exposure at 36,000 flight hours:

$$
n_{i,ref,36000}=6\,n_{i,ref,6000}
$$

For comparison with a real observation time $t_{real}$, the reference occurrence table shall be scaled to the same duration. When the conservative integer-floor convention is used:

$$
n_{i,ref,t}=\left\lfloor n_{i,ref,6000}\frac{t_{real}}{6000} \right\rfloor
$$

#### B.4 Calibration of the EFI constant

The calibrated constant $C'$ shall be computed from the 12,000-hour reference spectrum so that:

$$
EFI_{ref,12000}=\frac{1}{3}
$$

The constant shall be:

$$
C' = 3 \sum_j n_{j,ref,12000}
\left|LF_j-LF_{average,ref}\right|^k
$$

where $LF_j$ is the class-center load factor for class $j$.

#### B.5 Number of cycles to failure

For each load-factor class $i$, the equivalent number of cycles to failure shall be:

$$
N_i = C'\left|LF_i-LF_{average,ref}\right|^{-k}
$$

If $LF_i = LF_{average,ref}$ exactly, the corresponding amplitude is zero. The EFI contribution of that class is zero, and $N_i$ may be reported as infinite or not applicable to avoid division by zero in software output.

#### B.6 Real-flight EFI

The real-flight EFI shall be computed only from valid real aerodynamic recordings included in the processed data set:

$$
EFI_{real} =
\frac{1}{C'}
\sum_i n_{i,real}
\left|LF_i-LF_{average,real}\right|^k
$$

where $n_{i,real}$ is the occurrence table generated from valid aerodynamic measured data using Appendix A.

#### B.7 EFI ratio

For life-extension assessment over an observed valid aerodynamic recording duration $t_{real}$, the EFI ratio shall compare the measured EFI over that valid recording duration with the reference EFI normalized to the same duration:

$$
R = \frac{EFI_{ref,t}}{EFI_{real,t}}
$$

Using the same constant $C'$, this may be computed as:

$$
R =
\frac{
\sum_i
\left\lfloor
\dfrac{n_{i,ref,6000}t_{real}}{6000}
\right\rfloor
\left|LF_i-LF_{average,ref}\right|^k
}{
\sum_i
n_{i,real}
\left|LF_i-LF_{average,real}\right|^k
}
$$

when the conservative integer-floor convention is used.

#### B.8 Life-extension estimate

The estimated additional life beyond the certified service life shall be:

$$
t_{extension}=(R-1)t_{remaining\;ref}
$$

where $t_{remaining\;ref}$ is the time remaining until the certified service-life limit under reference-spectrum assumptions.

#### B.9 Treatment of non-instrumented, invalid, or excluded data

Non-instrumented, invalid, or excluded data are not part of the Kossira & Reinke spectrum-generation calculation defined in Appendix A and are not required inputs to the EFI calculation defined in Appendix B. The Kossira & Reinke and EFI software shall report the valid recording duration actually used.

Operational accounting for periods without valid SLM data, if required for a certified continued-airworthiness decision, shall be defined in the ICA, IOMM, or approved operational procedure. Such accounting is outside the core Kossira & Reinke spectra-generation and EFI-rate calculation defined in this appendix.

#### B.10 Required EFI outputs

The software shall report:

1. reference spectrum version and source;
2. reference occurrence table source, version, normalization duration, load-factor class definitions, and reference average load factor;
3. Kossira & Reinke algorithm version;
4. valid real aerodynamic recording duration used by the calculation;
5. reference average load factor;
6. real average load factor;
7. $b$, $k$, and $C'$;
8. reference EFI normalized to the valid real recording duration;
9. real measured EFI;
10. EFI ratio $R$;
11. estimated life extension when requested;
12. processing warnings and data-quality flags.

### 10. References

[1] Kossira, H. and Reinke, W. (OSTIV Publication XVI). "Determination of load spectra for the design of sailplanes."

[2] Kossira, H. (1982). "Determination of load spectra and their application for keeping the operational life proof of sporting airplanes." ICAS-Proc. 8/1982; ICAS-82-2.8.2, pp. 1330–1338.

[3] EASA Certification Memorandum CM-S-006, Certification, Type Design Definition, Material and Process Qualification for Composite Light Aircraft.

[4] Miner, M.A. (1945). Cumulative Damage in Fatigue. Journal of the Engineering Mechanics Division.

[5] Palmgren, A. (1947). A Probabilistic Theory of Cumulative Damage.

[6] Basquin, O.H. (1910). "The exponential law of endurance tests." Proceedings of the ASTM, Vol. 10, pp. 625–630.

[7] Derouineau, J.L. (OSTIV Publication). "Extension of Glider Life using Structural Life Monitoring."

[8] Kossira, H. and Reinke, W. "Festigkeit von modernen GFK-Konstruktionen für Segelflugzeuge - Bestimmung eines Belastungskollektives." IFL-IB 84-01, Technische Universität Braunschweig.

[9] Mandell, J. F., Samborsky, D. D., Agastra, P., Sears, A. T. and Wilson, T. J. (2010). *Analysis of SNL/MSU/DOE Fatigue Database Trends for Wind Turbine Blade Materials.* Sandia Contractor Report SAND2010-7052. Sandia National Laboratories.

[10] Samborsky, D. D., Agastra, P. and Mandell, J. F. (2012). "The SNL/MSU/DOE Fatigue of Composite Materials Database: Recent Trends." AIAA/ASME Wind Energy Symposium.

[11] Harris, B. (ed.) (2003). *Fatigue in Composites: Science and Technology of the Fatigue Response of Fibre-Reinforced Plastics*. Woodhead Publishing.

[12] Talreja, R. (1985). *Fatigue of Composite Materials*. Technomic Publishing.

[13] Bathias, C. (1999). *Fatigue of Materials and Structures: Application to Design and Damage*. Wiley.
