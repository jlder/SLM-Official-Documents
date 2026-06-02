## Structural Life Monitoring for Composite Gliders

### Methodology Report

*Based on: "Extension of Glider Life using Structural Life Monitoring" — J.L. Derouineau, FFVP / EGU* [7]

------

### 1. Purpose and Scope

This document describes the methodology used to assess and justify extended operational life for composite gliders using Structural Life Monitoring (SLM). The method computes real fatigue damage accumulation from onboard acceleration measurements and compares it against the damage accumulation limit established during type certification. As long as real cumulative damage remains below this limit, continued operation beyond the certified Service Life Limit is justified without modifying Type Certificate documents or certified structural limits.

The methodology is applicable only to composite gliders operated within the EASA CS-22 Utility-category flight envelope (some glider models considered for SLM were initially certified under the National Authority of the TC holder, but all Type Certificate Data Sheets are now listed under the EASA product list), for which a Service Life Limit has been established and for which the Kossira & Reinke Utility reference load spectrum is recognized as a basis for fatigue compliance. Aerobatic-category operation, aerobatic use, and any operation outside Utility-category limitations are excluded from the initial scope of SLM implementation.

------

### 2. Regulatory Basis

The method is consistent with the following regulatory framework:

- **CS 22.627** (Fatigue Strength): requires structures to be designed to avoid stress concentrations in normal service; does not explicitly mandate a specific life limit.
- **EASA CM-S-006**: endorses the use of Kossira & Reinke load spectra for fatigue analysis and testing of sailplanes.
- **CS-STAN 104b / Part ML**: governs installation of onboard recorders and maintenance requirements.

EASA has already accepted multiple means of compliance for CS 22.627, including full-scale fatigue testing and static overload testing. SLM is proposed as an additional means of compliance, consistent with Individual Aircraft Tracking methods validated over decades in military aviation.

------

### 3. Key Principles

**Service Life Limit and Certification Damage Limit**

The certified Service Life Limit (typically 12,000 flight hours) corresponds to a maximum allowable fatigue damage accumulation established at type certification. Certification is demonstrated against the safety-factored life: with a Safety Factor of 3, structural integrity is shown for 36,000 hours of equivalent fatigue. In Palmgren-Miner terms, the safety-factored reference exposure corresponds to the theoretical failure threshold, so the damage accumulated over the certified 12,000-hour life is one third of that threshold. The certification damage limit is therefore:
$$
\boxed{D_{limit} = \frac{1}{3}}
$$
This limit is not modified by the SLM method. SLM determines when this limit is reached under real operations, rather than under the conservative reference assumptions used in certification.

**Proportionality between load factor and structural stress**

Within the Utility-category certified flight envelope — defined by speed, configuration (flaps, airbrakes), and authorized mass loading — structural stress at all critical locations is proportional to the vertical load factor $N_z$. The manufacturer's design ensures that no critical stress exceeds the allowable for any authorized combination of these parameters. This proportionality holds during aerodynamic flight phases; it does not hold during non-aerodynamic phases (ground roll, winch launch), which are handled separately (see §4.2).

Importantly, the Palmgren-Miner rule is applied to stress *amplitudes* associated with load cycles, not to absolute static stress values alone. For a given critical location, if the stress amplitude is proportional to the load-factor amplitude within the authorized Utility-category flight envelope, the unknown proportionality coefficient is absorbed into the calibration of the damage model and cancels when the reference and real spectra are compared using the same method. The absolute value of this coefficient is therefore not required for the proposed damage-ratio approach. This does not mean that all structural locations have the same stress for a given load factor; it means that, within the authorized Utility envelope, load-factor variations provide a consistent proxy for the stress variations used in the fatigue comparison.

**High Cycle Fatigue regime**

Glider structures are designed so that operational stress levels remain well within the elastic domain of materials. The structure is therefore subject exclusively to High Cycle Fatigue (HCF), which justifies the use of the Basquin model for S/N curve representation throughout this methodology.

------

### 4. Methodology

#### 4.1 Reference Load Spectrum

The reference load spectrum for this methodology is the Kossira & Reinke Utility spectrum [2]. This is a deliberate initial-scope limitation: SLM is proposed at this stage only for gliders operated within Utility-category limitations. Aerobatic-category operation, aerobatic use, and any operation outside the Utility envelope are not credited under this methodology. The Utility spectrum is recognized by EASA (CM-S-006) as a basis for sailplane fatigue analysis. It is intentionally conservative: it covers the envelope of possible Utility-category glider usages and has built-in conservatism relative to typical operations.

The original Kossira & Reinke spectrum is published normalized to 6,000 flight hours. Because the certification damage limit is anchored at the 12,000-hour life (§3), the published occurrences are scaled to the required exposure time before use in the damage calculation. The original 1982 Kossira & Reinke spectrum is used rather than the more recent KoSMOS variant: KoSMOS omits low load factor variations to shorten ground-test duration, but those omissions are not appropriate when the reference spectrum is being compared cycle-for-cycle against a real measured spectrum.

#### 4.1.1 Use of the reference spectrum in the methodology

The Kossira & Reinke Utility reference spectrum is used whenever damage must be assessed against the certified reference basis. The detailed equations are introduced at the point where they are needed in the calculation:

1. The reference spectrum is scaled to the certified 12,000-hour life to anchor the damage model to the certification damage limit (§4.4).
2. Periods or phases without valid SLM data, including non-flight phases, are treated like non-instrumented operation and accounted at the reference damage rate (§4.2 and §4.4).
3. For life-extension projection, the damage produced by the reference spectrum is compared with the damage produced by real flights over the same real-flight duration. Because this duration may be much smaller than the duration of the published reference spectrum, the lower integer part of the scaled reference occurrences is used to keep the comparison fair and conservative (§4.5).


#### 4.2 Real Load Spectrum Acquisition

The vertical load factor $N_z$ is recorded continuously during flight using a tri-axial accelerometer located as close as possible to the Center of Gravity, in a rigid area near the wing spar. Proximity to the CG minimizes contamination from centripetal accelerations during attitude changes, while a rigid mounting area avoids local structural flexibility corrupting the measurement. Atmospheric turbulence and trajectory induce load variations at relatively low frequency, typically below 10 Hz.

Accelerometer requirements:

- Minimum sampling rate: 20 Hz
- 6-face calibration at each annual inspection to ensure recorder performance
- Installation calibration with the glider in level-flight attitude and wings level, so that the recorder-corrected vertical axis is aligned with the gravity vector in the reference flight attitude

Data is stored on onboard electronic memory and uploaded to a central repository after each flight.

**Non-flight phases.** During takeoff roll, landing roll, winch launch, and any other phase dominated by non-aerodynamic forces, the proportionality between vertical load factor and structural stress no longer holds. The accelerometer signal from these sequences shall therefore not be used to build the real aerodynamic load spectrum. These sequences are treated like non-instrumented operation and are accounted at the reference Kossira & Reinke damage rate corresponding to the Utility reference spectrum. This keeps the damage accounting conservative and avoids using accelerometer data outside the domain in which $N_z$ is a valid stress proxy.

#### 4.3 Load Spectrum Processing — Kossira & Reinke Counting Method

Both the reference and real spectra are processed using the same Kossira & Reinke counting method [2][8], ensuring a consistent and legitimate comparison. The method is described in Appendix A and summarized as follows:

1. Acquisition at $2^{10}$ resolution, corresponding to 1024 classes over a load factor range from -4g to +6g.
2. Hysteresis filtering.
3. Conversion to $2^5$ resolution, corresponding to 32 load factor classes.
4. Identification of successive peaks and valleys.
5. Recording of transitions between consecutive peaks and valleys in a 32×32 Markov transition matrix.
6. Transformation of the matrix to count exceedances above and below the mean load factor, producing the load spectrum: occurrences as a function of load factor level.

The use of the same counting method for both spectra is essential to the validity of the comparison. The choice of counting method affects the resulting occurrences; consistency eliminates this as a source of discrepancy.

#### 4.4 Damage Accumulation — Palmgren-Miner Rule

Cumulative fatigue damage is estimated using the Palmgren-Miner rule:
$$
D = \sum_i \frac{n_i}{N_i}
$$
where $n_i$ is the number of cycles at load factor level $i$, and $N_i$ is the number of cycles to failure at that level.

$N_i$ values are derived from the reference spectrum and material properties using the Basquin model. For conservative applicability across all composite glider structures, the worst-case GFRP Basquin exponent is used: $b = -0.15$. To simplify the notation, the positive fatigue damage exponent is defined as:
$$
\boxed{k = -\frac{1}{b}}
$$
For $b=-0.15$, $k=6.6$.

The $N_i$ expression, calibrated against the certification damage limit, is:
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
- $j$ — summation index running over **all** load factor levels of the reference spectrum. It is used inside the constant $C'$ to distinguish the summation over the whole spectrum from the single level $i$ at which $N_i$ is evaluated. The two indices range over the same set of load factor classes; different letters are used only to avoid confusion between the bound summation variable and the free index $i$.
- $n_{j,ref,12000}$ — number of cycles (occurrences) at load factor level $j$ in the **reference** Kossira & Reinke Utility spectrum, normalized to the certified life of **12,000 flight hours** and processed with the counting method of §4.3.
- $\mathrm{LF}_j$ — load factor value of class $j$; $\mathrm{LF}_i$ — load factor value of class $i$.
- $LF_{average,ref}$ — average load factor of the reference spectrum used to calibrate $C'$.
- $LF_{average,real}$ — average load factor of the valid real measured spectrum used to compute real damage.
- $b$ — Basquin S/N slope exponent.
- $k=-1/b$ — positive fatigue damage exponent used in the damage summations; $k=6.6$ for the conservative composite case.
- $C'$ — proportionality constant linking load factor amplitude to the number of cycles to failure. It is **not** a free parameter: it is fixed by calibrating the reference-spectrum damage against the certification damage limit $D_{ref,12000} = 1/3$.

Because the same calibrated constant $C'$, fatigue damage exponent $k$, load-factor class definition, and Kossira & Reinke counting method are applied to both the reference and the real spectra, the absolute value of the load-factor-to-stress proportionality coefficient cancels in the damage ratio and need not be known. The amplitude term is evaluated relative to the average load factor of the spectrum being assessed: $LF_{average,ref}$ for the reference spectrum and $LF_{average,real}$ for the real measured spectrum.

Real damage accumulation is then:
$$
\boxed{
D_{real}\;=\;\frac{1}{C'}\sum_i n_{i,real}\,\bigl|\mathrm{LF}_{i}-{LF_{average,real}}\bigr|^k
}
$$
For gliders instrumented partway through their life, total damage is:
$$
D_{total} = D_{not\;instrumented} + D_{real}
$$
where $D_{not\;instrumented}$ is computed using the reference spectrum normalized to the duration or operational exposure for which valid SLM data is not available, including non-flight phases treated as non-instrumented operation. $D_{real}$ requires no normalization as it already corresponds to the valid instrumented aerodynamic flight period. For a glider instrumented late in life, $D_{not\;instrumented}$ can dominate $D_{total}$, which is why early instrumentation is advantageous (§4.5).

#### 4.5 Life Extension Assessment

The Palmgren-Miner damage ratio $R$ quantifies the life extension potential:
$$
\boxed{R = \frac{D_{ref}}{D_{real}}}
$$
where both values are computed over the same observed flight duration $t_{real}$. Here $D_{ref}$ is the reference-spectrum damage normalized to $t_{real}$ — not the full-life value $D_{ref,12000} = 1/3$ of §3 and §4.4 — and $D_{real}$ is the measured damage of §4.4 over the same $t_{real}$.

To evaluate $R$ in practice, the reference and real spectra must cover the same exposure time. The published reference spectrum (normalized to 6,000 flight hours) is scaled down to $t_{real}$, and the floor function $\lfloor \cdot \rfloor$ is applied to the scaled reference occurrences to add conservatism (the real observation period $t_{real}$ being much shorter than 6,000 hours). The operational expression, using the fatigue damage exponent $k$, is:
$$
\boxed{R = \frac{\sum_i \left\lfloor \dfrac{n_{i,ref}\,t_{real}}{6000} \right\rfloor \,\bigl|\mathrm{LF}_i - LF_{average,ref}\bigr|^k}{\sum_i n_{i,real}\,\bigl|\mathrm{LF}_i - LF_{average,real}\bigr|^k}}
$$
where $n_{i,ref}$ and $n_{i,real}$ are the occurrences at load factor level $LF_i$ in the reference and real spectra respectively. This is the same computation as §4.4: substituting the $D_{ref}$ and $D_{real}$ expressions into $R = D_{ref}/D_{real}$, the constant $C'$ is identical for both spectra and cancels, leaving only the spectra and the fatigue damage exponent $k$.

The estimated life extension beyond the certified limit is:
$$
\boxed{t_{extension} = (R - 1) \times t_{remaining\;ref}}
$$
where $t_{remaining\;ref}$ is the flight time remaining until the certified 12,000-hour limit is reached under reference spectrum assumptions.

As an illustration, preliminary analysis of approximately 35 hours of flight data on an instrumented Janus B yielded a damage ratio of about 30 for composite (GFRP) parameters — corresponding to a potential life extension of several thousand hours for typical training and cross-country operations — and about 12 when aluminum parameters ($k = 5$) are used to assess metallic components. These figures are illustrative of the method rather than certified results. Operational implementation under this methodology shall use the Kossira & Reinke Utility reference spectrum and is limited to Utility-category operation.

Life extension is conditional on the assumption that future operations follow the same load pattern as those already observed. $R$ and $t_{extension}$ are therefore recalculated at each Airworthiness Review Certificate (ARC) renewal based on accumulated data. $R$ is highly sensitive to occasional high-load maneuvers: as an order of magnitude, a single 4g maneuver every two flight hours can reduce $R$ by more than an order of magnitude relative to gentle cross-country flying.

------

### 5. Applicability and Limitations

- Identical to all other methods for fatigue life identification, this method is valid only when the glider is operated within its certified Utility-category flight envelope (speed, configuration, mass distribution).
- Aerobatic-category operation, aerobatic use, and any operation outside Utility-category limitations are excluded from the initial scope of SLM implementation. If an aircraft is approved in both Utility and Aerobatic categories, SLM applicability is limited to operation within the Utility-category limitations.
- Life extension is dependent on actual usage. Aggressive flying or wide load factor excursions within the Utility envelope will reduce $R$ significantly relative to typical cross-country or training operations.
- The Basquin exponent $b = -0.15$, corresponding to $k = 6.6$, is conservative for GFRP structures and even more conservative for CFRP. The same method may be applied to metallic components using aluminum parameters ($b = -0.2$, $k = 5$), which is useful to validate inspection intervals for metallic parts.
- Non-flight phases, including takeoff roll, landing roll, winch launch, and any phase dominated by non-aerodynamic forces, are treated like non-instrumented operation. They are not derived from accelerometer cycles and are instead accounted at the reference Kossira & Reinke damage rate for the Utility reference spectrum (§4.2).
- The method does not substitute for visual or physical structural inspections, which continue throughout all phases of operation.

------

### 6. Concept of Operation associated with methodology

**Phase 1 — Instrumentation and Data Collection** *(below the certified life limit)* SLM recorder installed per CS-STAN 104b / Form 123. Annual 6-face calibration recorded in the aircraft logbook to verify data accuracy. Any flight or phase occurring without valid SLM data, including sensor fault, data corruption, missed calibration, or non-flight phases excluded from accelerometer-based processing, is substituted at the reference Kossira & Reinke damage rate for the corresponding duration or operational exposure.

**Phase 2 — Fatigue Evaluation at the Certified Life Limit** Dedicated structural inspection at 12,000 hours. Assessment of $D_{total}$ against the $D = 1/3$ limit. Continued operation authorized if inspection does not identify issues and  $D_{total} < 1/3$.

**Phase 3 — Operation Beyond the Certified Life Limit** Continuation of Phase 1 monitoring. Go/No-Go decision at each ARC renewal based on current $D_{total}$ and projected damage rate to next inspection. Recurring structural inspections at maximum 1,000-hour / 5-year intervals. Operation continues until $D_{total}$ reaches $1/3$.

------

### 7. Approval and Deployment Pathway

Since SLM is proposed as an additional means of compliance for fatigue life management, deployment should be supported by an approved certification pathway, such as an EASA Supplemental Type Certificate (STC) or another approval route accepted by the competent authority.

The approval package should include, as applicable:

- Certification Program
- Certification Review Item or equivalent agreement on the proposed means of compliance
- Methodology Report (this document)
- Instructions for Continued Airworthiness
- Installation, Operating and Maintenance Manual for the SLM recorder and associated data process

The certification basis should define the applicable glider models, Utility-category operating limitations, Kossira & Reinke Utility reference spectrum, material parameter assumptions, onboard recording requirements, data validation rules, treatment of non-instrumented and non-flight phases, damage computation process, inspection requirements, and go/no-go criteria for continued operation.

------

### 8. Appendix A — Kossira & Reinke Processing Rules

This appendix summarizes the minimum processing rules required to implement the Kossira & Reinke counting method consistently for both reference and real spectra [2][8].

1. **Acquisition and fine resolution.** The acquired load factor signal is represented at $2^{10}$ resolution, corresponding to 1024 classes over a typical load factor range from -4g to +6g. This gives a fine resolution of approximately 0.01g.
2. **Hysteresis filtering.** A new sample is retained only if its difference from the last retained sample exceeds the Kossira & Reinke threshold $DX$, typically $DX=10$ in the 1024-class representation, i.e. approximately 0.1g [8]. This prevents small oscillations near a class boundary from creating artificial fatigue cycles.
3. **Reduction to 32 classes.** Retained samples are converted to $2^5$ resolution, corresponding to 32 load factor classes over the same range. The corresponding class width is approximately 0.32g.
4. **Peak and valley detection.** Successive local maxima and minima are identified in the filtered 32-class signal. Only alternating peaks and valleys are used for Markov transition counting.
5. **Markov transition matrix.** Each transition from one retained peak/valley value to the next increments the corresponding cell of a 32×32 Markov matrix.
6. **Exceedance spectrum.** The Markov matrix is transformed into occurrences above and below the average load factor. The resulting spectrum gives the number of occurrences associated with each load factor level.
7. **Consistency rule.** The same class definition, filtering rule, peak/valley rule, Markov convention, and exceedance transformation shall be used for the reference spectrum and for real measured data. This consistency is essential because different counting methods can produce different occurrence distributions.

Implementation of the method requires the applicable Kossira & Reinke Utility reference occurrence table. That table should be included in the approved calculation package in machine-readable form.

------

### 9. References

[1] Kossira, H. and Reinke, W. (OSTIV Publication XVI). "Determination of load spectra for the design of sailplanes."

[2] Kossira, H. (1982). "Determination of load spectra and their application for keeping the operational life proof of sporting airplanes." ICAS-Proc. 8/1982; ICAS-82-2.8.2, pp. 1330–1338.

[3] EASA Certification Memorandum CM-S-006, Certification, Type Design Definition, Material and Process Qualification for Composite Light Aircraft.

[4] Miner, M.A. (1945). Cumulative Damage in Fatigue. Journal of the Engineering Mechanics Division.

[5] Palmgren, A. (1947). A Probabilistic Theory of Cumulative Damage.

[6] Basquin, O.H. (1910). "The exponential law of endurance tests." Proceedings of the ASTM, Vol. 10, pp. 625–630.

[7] Derouineau, J.L. (OSTIV Publication pending). "Extension of Glider Life using Structural Life Monitoring."

[8] Kossira, H. and Reinke, W. "Festigkeit von modernen GFK-Konstruktionen für Segelflugzeuge - Bestimmung eines Belastungskollektives." IFL-IB 84-01, Technische Universität Braunschweig.