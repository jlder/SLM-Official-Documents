

# 		    			Extension of Glider Life using

#  	    					Structural Life Monitoring



​								by   Jean-Luc Derouineau,
​				*Fédération Française de Vol en Planeur   /   European Gliding Union*



[toc]



## Abstract

The lifespan of a glider is limited by its susceptibility to fatigue damage. Repeated cyclic loading causes progressive damage accumulation, ultimately limiting its useful operational duration. The life limit currently imposed by EASA places a significant financial burden on glider clubs and contributes to composite waste, as no recycling solutions currently exist for end-of-life gliders.

This paper presents a Structural Life Monitoring (SLM) method to justify extended fatigue life, without revisiting certified structural limits or reopening Type Certificate documents. The method compares the EASA-recognized Kossira & Reinke reference load spectrum against the actual load spectrum measured during real flights, using the same Kossira & Reinke counting method for both, ensuring a consistent and legitimate comparison. Damage accumulation is estimated using the Palmgren-Miner rule. As long as real cumulative damage remains below the certification damage limit, continued operation is justified. The ratio between reference and real damage accumulation directly quantifies the potential life extension.

Preliminary results on an instrumented glider show a ratio of around 30, corresponding to potential life extensions of several thousand hours for typical training and cross-country operations. This is consistent with life assessments performed on certain gliders and similar composite structures in other industries. The method is conservative by design, maintains certified damage limits, and is compatible with EASA fatigue strength regulation requirements. A structured Concept of Operation and a certification pathway via EASA STC are proposed to support deployment.



## Acknowledgements

The development of this white paper benefited significantly from the input and support provided by multiple reviewers, representing considerable expertise in the domain of glider structure, fatigue, flight dynamics and analytics.
I would like to give special thanks to each of them for sharing their time and expertise.
Reviewers: (in alphabetical order)
Del Cid Liz, Kensche Christoph, Mesnil Guy François, Regis Olivier, Radespiel Rolf, Scherrer Matthieu, Scholz Werner.



## 1. Introduction

Prediction of aircraft life is critical for ensuring safety and cost-effectiveness:

- Cost is affected by life because of design solutions, material selection, and associated manufacturing. 
- Value is affected by life since used gliders depreciate suddenly when reaching their end of life. 

This is becoming a costly dilemma for small glider clubs which may not be able to replace their old gliders with more recent new or used models.
The carbon footprint of composite structures is also a growing environmental concern since glider manufacturers currently do not provide solutions for recycling their composite gliders.
Extending glider life would extend their value and reduce the environmental impact.

Before getting into the methodology discussion, it is important to understand some key definitions: Service Life Limit, Reference Load Spectrum, Fatigue Damage, S/N Curves and Safety Factor.

**Service Life Limit:** The Service Life Limit corresponds to the time a glider can fly, within the operational limits of its certified utilization category, without risking structural damage due to fatigue. Type Certificate holders may use different methods to demonstrate compliance with structural fatigue requirements, as accepted by the certification authorities. While these methods may vary, they all lead to an approved Service Life Limit. From an operational standpoint, it is this approved limit — not the method used to derive it — that governs how long a glider may remain in service. A typical glider Service Life Limit is 12,000 flight hours.

**Utilization Category / Reference Load Spectrum:** Gliders are certified to operate under a defined category. The Reference Load Spectrum corresponds to the load factor occurrences a glider may experience within its category over its entire Service Life. Reference Load Spectra have been established for the main glider categories, and are recognized by the certification authorities. Most gliders are certified under the Utility category, and the corresponding Kossira and Reinke spectrum [2] is recognized by the certification authorities.

**Fatigue Damage:** Aircraft structures are subject to variable loads throughout their service life, and repeated stress cycles can cause progressive structural deterioration — a phenomenon known as fatigue. Structural design aims to minimize stress concentrations, but fatigue damage accumulation must still be evaluated to ensure long-term structural integrity. One of the methods used in aerospace and accepted by EASA is the Palmgren-Miner rule, which combines load factor occurrences with the material's fatigue resistance to estimate cumulative damage. A Fatigue Damage value of 1 represents the theoretical failure threshold; designs are required to remain well below this limit over the intended service life.

**S/N Curves (Wöhler Curves):** Material fatigue resistance is characterized by the relationship between the stress amplitude applied to a specimen and the number of cycles it can sustain before failure. This relationship is represented graphically as an S/N curve, also known as a Wöhler curve, where S denotes the stress amplitude and N the corresponding number of cycles to failure. S/N curves are derived from laboratory testing. In the context of the Palmgren-Miner rule, the S/N curve is the link between the load spectrum and damage estimation: for each stress level in the Reference Load Spectrum, the corresponding number of cycles to failure is read from the S/N curve, allowing the contribution of each load cycle to the total accumulated damage to be quantified. Due to design and operational limits, gliders only suffer from high cycle fatigue.

**Safety Factor:** Because uncertainties are inherent in the way structural fatigue and its associated limits are calculated, it is standard aerospace practice to apply an overall Safety Factor, even when margins are already included in individual calculations. The Safety Factor is applied to the Service Life Limit that is targeted. This means that fatigue calculations must be performed against a target equal to the intended Service Life Limit multiplied by the Safety Factor. Aerospace typically uses a Safety Factor of 3. For example, a glider with a Service Life Limit of 12,000 flight hours must demonstrate structural integrity up to 36,000 hours of equivalent fatigue.

The load spectra, derived from Kossira & Reinke's seminal work [2], have become a key reference in defining load occurrence expectations for sailplane design and certification (EASA CS-22). These spectra were established using a compilation of a few hundred hours of real flight measurements performed on several gliders, flying in multiple conditions. The data and corresponding load factor occurrences have been extrapolated, using predefined operational profiles, to cover the envelope of all possible glider usages.

Recommendations by the European Union Aviation Safety Agency (EASA), as detailed in Certification Memorandum CM‑S‑006 [3], advocate for the use of these spectra for fatigue testing and structural analysis. In particular, the KoSMOS spectrum is the most recent version and includes omissions in the low load factor region, with no appreciable effect on damage calculation, to reduce testing time when actual laboratory fatigue tests are performed. 

EASA and other authorities have accepted several methods for compliance with the fatigue strength regulatory requirement (CS 22.627), including full-scale fatigue testing based on an accepted reference spectrum as well as static load tests with additional required safety margins [4] [5] [6].

The granted service life limit, using either of the previously described methods, sets the level of maximum acceptable damage accumulation. When using the Palmgren-Miner rule and a typical safety factor of 3, this means that the acceptable damage limit should not exceed 1/3.
Attempts have been made in the past, using modern modeling tools and recently available material fatigue data, to quantify and justify that the composite structures accumulate damage at a much lower rate compared to what was expected during initial certification [7]. However, reopening existing Type Certificate documents to reflect these findings is impractical.

The solution proposed in this paper uses Structural Health Monitoring principles to demonstrate that there are opportunities to justify operations beyond the original service life limit, without exceeding the maximum acceptable damage accumulation set during initial certification, eliminating the need to reopen Type Certificate (TC) documents.

This concept is already in use in military aviation to maximize service time of airplanes which have very dissimilar missions. Individual Aircraft Tracking (IAT), using onboard acceleration measurement, Palmgren-Miner damage accumulation, and comparison against a reference spectrum, has been validated on numerous defense aircraft types over more than 50 years.

For gliders certified under CS-22, the goal is to compute the real damage accumulation  using in-flight acceleration measurements. Damage accumulation can be computed using the Palmgren-Miner rule,  the number of cycles to failure, the reference load spectrum, and composite material properties.  As long as the damage accumulation stays below the certification damage limit, the operation of the glider can continue. The principle is shown in Figure 1.

![](.\life extesion graphic v1.jpg )

​						Figure 1: Life extension principle



## 2. Background and literature review

### 2.1 State Of the Art

#### 2.1.1 Introduction of life limit in glider industry

Until the introduction of composite materials, gliders were manufactured using wood, fabric and aluminum. The fatigue behavior of these materials is well understood, only requiring standard practice to avoid any concentration of stress above certification limits. At the time of certification of the older gliders, no explicit fatigue life analysis or testing was required.
The first composite gliders were manufactured in the late 1950s: fs 24 Phönix first flight was in 1957, followed by Hütter H 30 GFK in 1962 (which led to the Glasflügel Libelle) and Akaflieg Darmstadt D-36 in 1964. The D-36 led to the ASW 12 (Waibel / Schleicher), the Cirrus (Holighaus / Schempp-Hirth) and LS1 (Lemke / LS) sailplanes which were then built in series. By the 1970s, composite materials became the standard in high-performance glider manufacturing, and all modern gliders today are made with advanced composite structures.

The glider community has been a pioneer in the use of composite materials, but industry's relative inexperience and limited understanding of fatigue behavior led some certification authorities to introduce a life limit. This 12,000-hour limit, which was set by LBA (Luftfahrt-Bundesamt), remains the standard life limit today under EASA.
It should be noted that, even if authorities like LBA imposed a relatively short limit on new designs, other authorities such as TRAFI [8]  (Finland) and DGAC (France) approved much higher limits or even no limit (PIK20, Centrair C101).

#### 2.1.2 Current state and possible evolutions

Today, the EASA has maintained the 12,000-hour life limit, although the CS 22.627 (Fatigue strength) only requires that "structure must be designed, as far as practicable, to avoid points of stress concentration where variable stresses above the fatigue limit are likely to occur in normal service".

In the glider industry, few full-scale fatigue tests have been performed. In most cases, the glider manufacturers have been complying with the requirement using the EASA accepted static overload test.
However, there has been one particularly interesting full-scale fatigue test performed in the 1990s, in Australia, on a Janus B wing [9]. The glider was not new and one wing had substantial repairs. Some defects were intentionally left unrepaired and some defects were created to simulate typical incidents (such as wing damage during out-landing). The conclusion was clear, confirming that there was no significant damage accumulation on the wing without repair and that only the non-repaired  sections had substantial growth of  minor damage. However, the propagation rate of delamination was slow and could be easily detected during the aging/fatigue inspection, which is mandatory at 6,000, 9,000, 10,000 & 11,000 hours.

The experience gained in the aerospace industry, as well as other industries like wind turbines, from inspection of aging composite structures, improved fiber characterization and better modeling, has validated the excellent fatigue behavior of composite airframes. This confirms that the historical 12,000-hour life limit imposed on gliders is extremely conservative as already demonstrated in a previous analysis "Numerical Comparison of Glider Load Spectra" [7].

Even if recent analyses have identified structural margin opportunities, it is not practical to reopen structure analysis for gliders certified 30 or more years ago. However, thanks to better understanding of glider operational usage and the corresponding composite materials damage accumulation due to fatigue, our proposed method provides a solution to extend the life of gliders, without changing the certification damage accumulation limit associated with the safe life limit (12,000 hours).



### 2.2 Reference load spectrum, distribution occurrences and application to operational life assessment

The load spectra developed by Kossira & Reinke are foundational in sailplane design. In their seminal work, *“Determination of load spectra for the design of sailplanes”* [1], they established a methodology for deriving a reference load spectrum that includes both the stress levels and the occurrence frequency (distribution) of these load events.
To establish their load spectra, they instrumented gliders which were flown in different conditions, with the goal of being representative of the envelope of all possible flight usages. Because they could only fly for a limited time, it was necessary to scale the data to be representative of 6,000 or 12,000 flight hours required for certification. They used an extrapolation method which not only scales the occurrences as a function of time, but also increases the maximum and minimum load cycle values. While this extrapolation method is understandable, from a statistical point of view to account for the lack of variability due to reduced flight time, it might be a source of over-estimation.

The counting method used by Kossira & Reinke is very similar to the "peak and valley" solution [10], with the addition of a simple filter to avoid counting minor load factor variations, and the optional use of a Markov transition matrix to count occurrences. These occurrences specify the expected number of cycles at various stress levels over a defined operational period, and form the basis for fatigue life predictions. However, it should be noted that these spectra have been developed to cover the envelope of all possible operations and have built-in conservatism compared to most typical operations.
The KoSMOS spectrum (Kollektiv für Segelflugzeuge, Motorflugzeuge und Motor-Segler, i.e. load collective for sailplanes, aeroplanes and powered gliders) is based on the original data from Kossira & Reinke with omissions of the low level stress variations. The goal is to significantly reduce test time when the spectrum is used for ground tests. Because our goal is to eventually compare the reference spectrum to the actual spectrum flown by a given glider, it is more suitable to use the original Kossira & Reinke spectra from their 1982 publication [2], which do not have these omissions.

Kossira & Reinke published multiple spectra corresponding to different utilization categories. The initial analysis presented in this paper uses the flight-only spectrum, which excludes simple aerobatics and ground operations. While most gliders are certified under the Utility category — which permits limited aerobatics — this conservative choice ensures that the results represent a lower bound of the potential life extension. Including simple aerobatics and ground operations would add occurrences at higher load factors, increasing the reference damage accumulation and yielding a more favorable damage ratio. Figure 2 is a representation of the Kossira & Reinke flight-only spectrum, normalized at 6,000 flight hours.



<img src=".\Kossira spectra flight only 6000FH v1.jpg" style="zoom:80%;" />

​			*Figure 2: Kossira & Reinke flight-only spectrum normalized for 6,000 Flight Hours [2]*
​                                                   *(x axis: occurrences / y axis: load factor)*

Kossira & Reinke’s subsequent work, *“Determination of load spectra and their application for keeping the operational life proof of sporting airplanes”* [2], extends these concepts to operational life assessment. The occurrence distribution, in this framework, enables the calculation of cumulative damage via cycle counts.



### 2.3 Kossira & Reinke counting method

Multiple counting methods have been developed over time, e.g. level crossing, peaks & valleys or Rainflow [10], and there are differences in the resulting occurrence calculations. The goal of this study is to compare the damage accumulation between the reference  spectrum and real flight spectra, and use the counting method developed by Kossira & Reinke [2] for their own spectra to compute occurrences for the real flight spectra.

#### 2.3.1 Kossira & Reinke counting method principle

The Kossira & Reinke spectra were developed in the eighties to provide glider designers with load spectra which could be used for fatigue analysis, tests, and life justifications [2].

These spectra  are referenced by EASA in their certification memorandum (CM-S-006 Issue 01 issued 20 January 2015) [3].

To establish these spectra, gliders have been instrumented to record the stress on the wing during multiple phases of flight. 
Using the limited digital technology available at that time, the acquisition and processing were relatively simple: 

1. Converting the wing loading, calculated with the spar bending moments divided by a reference bending moment, into digital classes of 2<sup>10</sup> and  2<sup>5</sup> precision, 
2. simple filtering to reduce the effect of small load factor variations (noise),
3. identifying maxima and minima in the smaller  2<sup>5</sup> class (maxima and minima are also called peaks & valleys), 
4. filling a Markov transition matrix using "from stress/load factor"  to "to stress/load factor" transitions which correspond to transitions from minimum (valley) to maximum (peak) as well as  maximum (peak) to minimum (valley),
5. transforming the Markov matrix to count exceedances above and below the average load factor level,
6. summing the cells of the rows of the transformed Markov matrix to create the more user friendly Load Factor as function of occurrences exceedances graphic.

This final step provides the representation in Figure 2 and Figure 3 which are commonly called load spectra and which can be used for damage and life analysis. It is interesting to note that, while the values are slightly different, the shape and the average values between the reference and real spectra are consistent. 



<img src=".\spectrum_ventus.jpg" style="zoom: 67%;" />

​			Figure 3: Examples of Kossira & Reinke flight-only spectrum and real flights Ventus spectrum
​								 ( x axis: occurrences /  y axis: load factor)



#### 2.3.2 Acquisition and classes

The sensor's signal, representing the glider body vertical axis load factor, is converted to digital values using  2<sup>10</sup> precision (signal is quantified into 1024 classes). With a typical load factor range of -4g to +6g, the difference between two adjacent classes is small (approximately 0.01g). Analyzing the transitions using this accuracy results in a high number of small transitions, which have no real value for fatigue and life analysis.
The solution proposed by Kossira & Reinke is to use a sub class using 2<sup>5</sup> precision ( signal quantified in 32 classes). With such resolution, the difference between two adjacent 32-class values is approximately 0.32g which is more representative for fatigue and life analysis.

<img src=".\class_32_1_to_32_-4_to_6.jpg" style="zoom:80%;" />

​											Table 1: 32-Class definition



#### 2.3.3 Filtering

Using data in the 32-class format is simple but has a negative effect since it amplifies small signal variations when these variations occur at the limit of the 32-class transitions. For example, with an input range of -4g to +6g,  if the value of the input signal is 0.95g, the 1024-class value is 507 and the 32-class value is 16. If the signal increases slightly by e.g. 0.08g, the 1024-class value becomes 516 and the 32-class value 17. If the input signal oscillates between these values, the 32-class values also oscillate between 16 and 17, which means that a small 0.08g input signal variation is turned into a large 0.32g variation when converted to 32-class. To avoid these undesired 32-class variations induced by small input signal variations, Kossira & Reinke introduced a simple filtering solution by only taking into account a new sample, if the difference between this new sample and the last recorded sample exceeds a threshold DX, in the 1024-class.  In their experimentations, Kossira & Reinke have used DX=10 [11], which means that the difference between previous sample and current sample has to be at least ~0.1g , for current sample to be processed. Figure 4 provides an illustration of the filtering/hysteresis proposed by Kossira & Reinke [2].

![](.\class 1024 32  filter v1.jpg)

​									Figure 4: Kossira & Reinke filtering solution



#### 2.3.4 Maxima and minima (peaks and valleys)

When the input data is filtered and reduced to the 32-class, it is straightforward to identify the minima and maxima in the data stream. The resulting data stream is a succession of minima and maxima in alternation, also called peaks and valleys, as shown in Figure 5.

<img src=".\peaksandvalleys.jpg" style="zoom:80%;" />

​							Figure 5: Maxima & Minima  /  Peaks & Valleys



#### 2.3.5 Markov transition matrix

The peaks and valleys data stream obtained from the previous steps is used to fill the Markov transition matrix. Because the data is in the 32-class format, the matrix size is 32 x 32. The columns of the matrix correspond to the "from" load factor of a transition and the rows of the matrix correspond to the "to" load factor of the transition. The peaks and valleys are processed by taking two consecutive values which respectively correspond to the "from" load factor and the "to" load factor. The corresponding cell of the Markov transition matrix is incremented. Figure 6 provides an example of a Markov matrix from a single flight.

<img src=".\Markov1.jpg" style="zoom: 67%;" />

​							Figure 6: Example of Markov transition matrix
​					( x axis: "**from**" level transition /  y axis: "**to**" level transition )



#### 2.3.6 Load factor as function of occurrences spectrum representation

To convert the Markov transition matrix data to the more traditional load factor as function of occurrences spectrum representation, it is necessary to first determine the average load factor value for the considered flight sequence(s).
Then compute how many transitions went through a given load factor above and below the mean value:

1. for each of the load factor cells above the mean value and above diagonal, compute the sum of all the occurrences at and above the considered cell (Figure 7 red/black example)

2. for each of the load factor cells below the mean value and below diagonal, compute the sum of all the occurrences at and below the considered cell (Figure 7 green/light gray example).

   ​									<img src=".\Markov1to2.jpg" style="zoom: 67%;" />

​					Figure 7: Calculation of the number of transitions through a given cell
​						( x axis: "**from**" level transition /  y axis: "**to**" level transition )



For a given load factor level, sum all the occurrences to obtain the spectrum table and graphic representation, as seen in Figure 8 and Figure 9.

<img src=".\Markov2toSpectrum.jpg" style="zoom:67%;" />

​			Figure 8: Calculation of the total number of occurrences for every load factor level
​				( Left  =  x axis: "**from**" level transition /  y axis: "**to**" level transition
  				Right = x axis: number of occurrences / y axis: load factor )



![](.\Janus 6000 FH.jpg)

​					Figure 9: Example of load factor spectrum from a glider real flights in green/black 
​	with Kossira & Reinke reference flight-only (no aerobatics) spectrum in red/gray normalized at 6,000 flight hours
​							(horizontal axis: occurrences  /  vertical axis: g load)



### 2.4 Real load spectrum in glider operations

In actual glider operations, load conditions deviate from the conservative assumptions of reference models. Factors such as pilot technique, environmental variations, and operational profiles lead to a real load spectrum that often exhibits fewer or less severe load events than those predicted by the Kossira & Reinke distribution. The accelerations measured during actual flights are processed using the Kossira & Reinke counting method to provide these real load spectra.



### 2.5 Fatigue damage accumulation: the Palmgren-Miner rule

Since the spectra have been established with the same counting method, it is reasonable to use the same solution to estimate and compare the fatigue or damage corresponding to each spectrum.
The Palmgren-Miner rule [12] [13] provides a linear damage accumulation model for fatigue, expressed as:
$$
D = \sum_i \frac{n_i}{N_i}
$$
where $n_i$ is the number of cycles at a specific stress level, and $N_i$ is the number of cycles to failure at that level. When $$D$$ reaches the value 1, the structure is considered to have failed.
In the sailplane fatigue context, damage accumulation $$D$$ corresponds to the sum of individual damages computed at each considered load factor level (stress level), either from operations (real load spectrum) or from the reference spectrum. Each individual damage, at a given stress level, is the ratio between the occurrences applied to the structure at that level ($$n_i$$) and the number of occurrences required to fail the structure at that same stress level ($$N_i$$). 

It is therefore possible to estimate damage accumulation from a given spectrum to ensure the value stays below a certain limit.
When multiple spectra are available,  and the respective damage accumulations are estimated over the same exposure time, it becomes possible to directly compare them and eventually estimate life extension when the real flight spectrum is less severe than the reference spectrum.



### 2.6 Number of cycles to failure ($$N_i$$)

For a given load spectrum, either reference or from actual flight measurements, the occurrences at a given stress level $$n_i$$  are known. To estimate the damage accumulation $$D$$, corresponding to that spectrum, we only need $$N_i$$, which is the number of occurrences required to fail the structure at each load factor/stress level.

#### 2.6.1 Material fatigue representation - $$S/N curve$$

Modeling fatigue is instrumental in understanding how materials  behave under occurrences of loading. This is vital for industries such as  aerospace, automotive, and construction. One  tool used to represent fatigue data is the **S-N curve**, originally known as the Wöhler curve. 

Wöhler's work has been at the root of modern fatigue analysis and testing. It introduced the first graphical representation of stress vs. cycles to failure and is now commonly referred to as the S-N curve as shown in Figure 10.

An S-N curve provides a representation of the relationship between the stress amplitude (**S**) applied to a material and the number of cycles to failure (**N**) it can endure. 

- $$S\;:$$ Stress a material experiences during a single cycle.
- $$N\;:$$ Total number of cycles a material can withstand before failing.

For fatigue analysis and demonstrations, there is a direct correlation between stress cycles and load factor cycles due to the stress considered: structure flexion under load factor. 

<img src=".\SN_curve simple v1.png" style="zoom:67%;" />

​											Figure 10: Typical Wöhler curve



#### 2.6.2 Material fatigue representation - Basquin model

To be able to perform fatigue and life calculation, Basquin [14] has proposed a simple mathematical model, mainly focusing on the high cycle fatigue of the $$S/N$$ curve:
$$
\sigma_{a} \;=\;\sigma'_f\;\Bigl(\frac{2N}{\varepsilon'_F}\Bigr)^{b}
$$
where:
– $σ_a$ : stress amplitude
– $σ'_f$ : fatigue strength coefficient (≈ intercept of the $$S/N$$ curve)
– $N$ : number of cycles to failure
– $ε'_F$ : fatigue ductility coefficient (scales the cycle axis)
– $b$ : fatigue strength exponent (slope of the S–N curve)

With the exception of $$N$$, all material property parameters are constants.
For this purpose, the Basquin equation simplifies to:
$$
\sigma_{a} \;=\; C \; N^{b}
$$
with $$C$$ constant : 
$$
C\; = \sigma'_f\;\Bigl(\frac{2}{\varepsilon'_F}\Bigr)^{b}
$$
It expresses the stress‐amplitude $σ_a$ required to produce failure in $N$ cycles as a power‑law function of $N$.

This model is only valid for the high cycle fatigue of the $$S/N$$ curve, and is not an issue for this application as, by design margins, a glider does not operate into the low cycle fatigue.  At the other end of the curve, the Basquin model is very conservative since it does not consider the asymptotic part of the $$S/N$$ curve in the very low stress variations region.



#### 2.6.3 End of life damage accumulation estimation

By design, a glider has a finite fatigue life potential. While the glider is operated, this potential is consumed by the occurrence of the load variations (cycles).
The reference load factor spectrum and the real load factor spectrum are two examples of how the occurrences are distributed as a function of the load factor as well as their frequency.
When the potential is consumed, the component(s) subject to fatigue could fail. When the Palmgren-Miner rule is used as a way to estimate damage accumulation, this means the corresponding value  $$D$$ has reached $$1$$.

Certification requirements and common practice incorporate a safety factor of 3, so that if a life of e.g., 12,000 hours is targeted, the calculations and validations should be performed for a duration of 36,000 hours.

Therefore, when using Kossira & Reinke as the reference spectrum, and Palmgren-Miner as a way to estimate damage, the damage accumulation is:
$$
D_{ref,36000}\;=\;\sum_i \frac{n_{i,ref,36000}}{N_i}\; = 1
$$
when the spectrum of occurrences corresponds to 36,000 hours exposure time,
and:
$$
D_{ref,12000}\;=\;\sum_i \frac{n_{i,ref,12000}}{N_i}\; = \frac{1}{3}
$$
when the spectrum of occurrences corresponds to 12,000-hour exposure time.

$$
\boxed{D = \frac {1}{3}}
$$
This damage value corresponds to 12,000-hour life potential limit for damage accumulation.



#### 2.6.4 Number of cycles to failure $${N_i}$$ from reference spectrum and material properties

Local stresses can be considered linear with the load factor around the average load factor:
$$
σ_{a,i} \;\propto\;|LF_i - {LF_\text{average}}\bigr|
$$
with  $${LF_i}$$  the load factor and $${LF_\text{average}}$$  the average load factor during the exposed time.
Using the Basquin model, with a constant $$C'$$ which can be derived from the certification condition using the reference spectrum:
$$
|LF_i - {LF_\text{average}}\bigr|\propto\  C'\,N_i^b
$$

$$
N_i \;=\; C'\;\bigl|LF_i - {LF_\text{average}}\bigr|^{1/b}
$$

with $C'$ being a proportionality constant which can be calculated using the reference damage accumulation: 

$$
D_{ref,12000}\;=\;\sum_i \frac{n_{i,ref,12000}}{N_i}\; = \frac{1}{3}
$$


$$
with  \; N_i \;=\; C'\;\bigl|\mathrm{LF}_i - {LF_{average}}\bigr|^{1/b}
$$

$$
\sum_i \frac{n_{i,ref,12000}}{N_i} = \frac{1}{3}
\quad\Longrightarrow\quad
\sum_i \frac{n_{i,ref,12000}}{\,C'\bigl|LF_i - {LF_\text{average}}\bigr|^{1/b}\,} = \frac{1}{3}.
$$

$$
\sum_i \frac{n_{i,ref,12000}\,|\mathrm{LF}_i-{LF_{average}}|^{-1/b}}{C'} \;=\;\frac {1}{3}.
$$

$$
\frac{1}{C'}\,\sum_i n_{i,ref,12000}\,\bigl|\mathrm{LF}_i-{LF_{average}}\bigr|^{-1/b} \;=\;\frac{1}{3}
$$

$$
\quad\Longrightarrow\quad
C' \;=\;3\;\sum_i n_{i,ref,12000}\,\bigl|\mathrm{LF}_i-{LF_{average}}\bigr|^{-1/b}.
$$

The complete expression to calculate the $$N_i$$ values which can be used to assess cumulative damage can be written as:
$$
\boxed{%
N_i \;=\; \underbrace{3 \;\sum_j n_{j,ref,12000}\,\bigl|\mathrm{LF}_j-{LF_{average}}\bigr|^{-1/b}}_{C'}\;\bigl|\mathrm{LF}_i-{LF_{average}}\bigr|^{1/b}\,.%
}
$$
For a given spectrum $$n, \;LF \;and \;LF_{average}$$ are known, allowing calculation of $$C'$$ and subsequently all the  $$N_i$$ values for each load factor of the spectrum.
These $$N_i$$ values are only functions of the spectrum and the slope of the $$S/N$$ curve  $$b$$, as the Kossira & Reinke reference spectrum is known. If a conservative $$S/N$$ slope $$b$$ value is chosen to cover all types of composite glider structures, the resulting $$N_i$$ values would become a reference usable for all damage estimations.



## 3. Methodology

### 3.1 Data acquisition

#### 3.1.1 Load cycle acquisition using accelerometers

**From bending moment to load factor — establishing proportionality**

To establish their spectra, Kossira & Reinke originally instrumented gliders with strain gauges on the wing spar at the root, measuring the spar bending moment $M_{br}$. A reference bending moment $M_{br1g}$ was established by flying in calm air with a stable trajectory (vertical acceleration ≈ 1g). Bending moments measured during flight were then divided by this reference value, yielding the normalized ratio $\frac{M_{br}}{M_{br1g}}$, which represents the wing loading in flight.

When the glider is primarily subject to aerodynamic forces, this ratio is directly proportional to the vertical load factor $N_z$, which can be measured more practically using an accelerometer. This proportionality is the foundation of the SLM approach: if stress at any critical structural location is proportional to the load factor, then measuring load factor is sufficient to estimate fatigue damage accumulation.

**Validity of the proportionality within the certified flight envelope**

One may argue that the relationship between load factor and local stress is not unique — that the maximum stress could occur at different locations on the structure depending on the aerodynamic and mass distribution along the wing, and that the coefficient of proportionality between stress and load factor is therefore unknown.

This objection is valid in general, but does not apply when the glider is operated within its certified flight envelope. By design, the manufacturer has ensured that, for any combination of speed, flap and airbrake configuration, and mass loading within the authorized range — covering fuselage weight (pilots) and wing mass (including water ballast) — the resulting stress at all critical structural locations remains below the maximum allowable. The structural design therefore implicitly bounds the stress at every critical point as a function of load factor, within the operational envelope.

This is further reinforced by the use of load factor limits in glider operational documentation. The maximum and minimum load factor limits published in the Flight Manual are precisely the operational expression of this design constraint: they are the values beyond which structural stress would exceed acceptable levels. As long as the glider is flown within these limits and within the authorized configuration and mass envelope, load factor is a valid and sufficient proxy for structural stress.

Furthermore, it is important to note that the absolute value of the proportionality coefficient between load factor and local stress is not required. The Palmgren-Miner damage accumulation relies on stress amplitudes — that is, the variation of stress between successive peaks and valleys — rather than absolute stress values. Since stress is proportional to load factor within the authorized flight envelope, stress amplitude is equally proportional to load factor amplitude. The proportionality coefficient therefore cancels out when computing the damage ratio between the reference and real spectra. What matters is not the magnitude of the coefficient, nor where on the structure the maximum stress occurs, but simply that the glider is operated within its authorized flight envelope, ensuring that load factor variations remain a consistent and valid representation of stress variations throughout the structure.

Although not explicitly documented in their work [11], this is probably the reason why Kossira & Reinke only instrumented the glider under test at the root of the wing spar.
They were looking for stress variations centered around the average flight stress (i.e. $\frac{M_{br}}{M_{br1g}}$).

**Accelerometers as a practical substitute for strain gauges**

This equivalence makes accelerometer-based recording a cost-effective and practical substitute for strain gauges in the context of SLM. The accelerometer should be located as close as possible to the Center of Gravity (CG) to minimize contamination from centripetal accelerations during attitude changes. Practically, a location in the rigid structure close to wing spar intersection, within the fuselage is appropriate.

**Non-flight phases**

The proportionality between load factor and spar stress holds during normal flight phases. During ground rolls or winch launches, significant non-aerodynamic forces are present and the relationship no longer holds directly. Until dedicated flight physics models are validated for these phases, a conservative fixed contribution to the fatigue spectrum can be added, based on the same assumptions Kossira & Reinke applied for ground maneuvers and winch launches. The approach adopted for the initial experimentation is described in section 3.1.2.

#### 3.1.2 Data acquisition for experimentation

Real flight load factor $$N_z$$ is recorded in real time using accelerometers  located on the wing spar (close enough from CG and very rigid), and electronic memory (e.g. SD card).
This data is processed using the Kossira & Reinke method to build the real flight load spectra. Using the same method as Kossira & Reinke for their reference spectra is important to make comparison between real and reference spectra legitimate.

During the initial experimentation, the takeoff and landing roll are treated as normal flight sequences. This is conservative since the Kossira & Reinke flight-only reference spectrum does not include ground operation phases. Any load factor occurrences recorded during takeoff and landing rolls are added to the real spectrum without a corresponding contribution in the reference spectrum, resulting in a lower Palmgren-Miner ratio at those load factor levels, and therefore a more conservative overall life extension estimate. No winch takeoffs are being planned with the experimentation gliders but, if this was the case, the same Kossira & Reinke assumptions would be used to add the corresponding load cycle occurrences to the experimentation glider spectrum. This is believed to cover for the limitations of using accelerometers instead of strain gauges.

Since most of the energy from turbulence (CS 22.341) or glider movement is below 10 Hz, the accelerometers should be filtered with a cutoff of at least 10 Hz, requiring a minimum sampling rate of 20 Hz. Accelerometer calibration should be checked before every flight when the glider is static to make sure the magnitude of the gravity measured on the 3 axes is ~1g.




### 3.2 Load spectrum analysis

Two load spectra are defined:

- **Reference Load Spectrum:** Based on Kossira & Reinke  (as recommended by the European Union Aviation Safety Agency), this reference spectrum includes the stress levels  (load factor) and their corresponding distribution occurrences (Figure 2).
- **Real Load Spectrum:** Derived from flight data, representing the actual occurrences of various stress levels during operations. To be consistent with the reference spectrum, the Kossira & Reinke counting method (§ 2.3) shall be used.
  Within the scope of the initial experimentation, all phases of flight were included (takeoff, flight and landing). 

To allow comparison between spectra,  the same load factor range should be used, and the respective cycle counts $n_i$ should be normalized to the same flight duration.




### 3.3 Application of the Palmgren-Miner rule to estimate life extension

#### 3.3.1  Damage level condition to continue operation beyond the 12,000-hour limit

Since we know the real spectrum and the number of cycles to failure $$N_i$$, it is possible to calculate the value of the damage accumulation from the $$real$$ spectrum using flight recording.
$$
D_{real}\;<\; \frac{1}{3}
$$

$$
where \;\;N_i \;=\; C'\;\bigl|LF_{i} - {LF_\text{average,real}}\bigr|^{1/b}
$$

$$
\boxed{
D_{real}\;=\;\frac{1}{C'}\sum_i \frac{n_{i,real}}{\bigl|\mathrm{LF}_{i}-{LF_{average,real}}\bigr|^{1/b}}}
$$

$$
where \;\;C' \;=\;3\;\sum_i n_{i,ref,12000}\,\bigl|\mathrm{LF}_{i}-{LF_{average,ref}}\bigr|^{-1/b}
$$

As long as $$D_{real}$$ stays below  $$\frac{1}{3}$$, the glider can continue operations.

In reality, gliders will only be instrumented late in their life. The damage accumulation will be a combination of reference damage (when the glider is not instrumented) and real damage (when the glider is instrumented):  
$$
D_{total} = D_{glider \; not \;instrumented} + D_{glider \; instrumented}
$$
where $$D_{glider  \; not \; instrumented}$$  is computed using the reference spectrum normalized for a duration equal to the time during which the  glider was flying without instrumentation.
and where $$D_{glider \; instrumented}\;=\;D_{real}$$  is computed using the real flight occurrences. There is no need to normalize as it corresponds to  the duration when the glider was instrumented.
The condition is that the glider can stay in operation as long as $$D_{total}$$ stays below  $$\frac {1}{3}$$ . 



#### 3.3.2  Life extension estimation

Once the damage from actual flights has been computed using the Palmgren-Miner rule, it is possible to estimate how much longer a glider can operate beyond the certified 12,000-hour life limit, with the important assumption that the real usage continues with the same load pattern as the flights already performed.

##### 3.3.2.1 Damage accumulation rate

As damage accumulation is assumed to be linear with respect to time under a given load spectrum, as defined by the Palmgren-Miner rule, the total damage a glider accumulates over time can be expressed as:
$$
D = t \cdot D_{\text{unit}},
$$

where:

$$D$$  is the total accumulated damage,

$$t$$  is the flight time,

$$D_{unit}$$  is the damage per hour under a specific load spectrum.



##### 3.3.2.2 Remaining real life and Palmgren-Miner ratio

Let:

$$D_\text{unit real}$$  = damage accumulated from actual flight load spectrum in 1 hour

$$D_\text{unit ref}$$ = damage predicted by the certified Kossira & Reinke load spectrum in 1 hour

$$t_{remaining\;ref}$$ = flight time remaining until the certified 12,000 hours are reached (under reference spectrum usage)

$$t_{remaining\;real}$$ = estimated remaining life under actual usage

$$D_{\text{remaining}}$$ = damage potential remaining until the certification limit $${D = \frac {1}{3}}$$ is reached

For a given remaining damage potential $$D_{\text{remaining}}$$, the time required to consume it differs based on the spectrum used:

- Under the certified reference spectrum:
  $$
  t_{\text{remaining ref}} = \frac{D_{\text{remaining}}}{D_{\text{unit ref}}}
  $$

- Under the actual (real) measured flight data:
  $$
  t_{\text{remaining real}} = \frac{D_{\text{remaining}}}{D_{\text{unit real}}}
  $$

and define the Palmgren-Miner damage ratio \(R\) as:
$$
\boxed{R = \frac{D_{\text{unit ref}}}{D_{\text{unit real}}}}
$$

Substituting into the previous expression:
$$
t_{\text{remaining real}} = t_{\text{remaining ref}} \times R
$$

Thus, if real-world flights result in significantly lower damage per hour than the conservative certified assumption, the remaining life is proportionally extended.




##### 3.3.2.3 Additional life

The additional flying time enabled by lower real-world fatigue loads is:
$$
t_{extension} = t_{remaining\;real} - t_{remaining\;ref}
$$

$$
\boxed {
t_{extension} = (R - 1) \times t_{remaining\;ref}
}
$$
To ensure the Palmgren-Miner ratio $$R$$  is valid, both damage values must be computed over the same duration (e.g., the same number of flight hours).

For our  specific problem, $$R$$ should be estimated using the data from the real spectrum, which by definition has a duration of $$t_\text{real}$$ , and the data from the reference spectra, normalized to the same  $$t_{real}$$ hours:

- $$t_{real}$$ = duration of real flight data collected (in hours)
- $$D_{real}$$ = damage accumulated from actual flight load spectrum in  $$t_{real}$$ hours
- $$D_\text{ref}$$ = damage predicted by the certified Kossira & Reinke reference load spectrum in  $$t_{real}$$ hours

$$
D_\text{ref} = D_\text{unit ref}\times t_\text{real}
\\
D_\text{real} = D_\text{unit real} \times t_\text{real}
\\
R = \frac{D_\text{ref}}{D_\text{real}}
$$

If the reference spectrum has been calculated over the typical 6,000 flight hours, for $$R$$ calculation, it should be normalized to the  time used for real spectrum observation  $$t_\text{real}$$ , using $$⌊ \frac{ni, ref \times t_{real}}{6000}⌋$$. The purpose of using the lower  integer part of a real number (denoted **⌊   ⌋**), is to provide additional conservatism when adjusting the $$n_i$$ of the reference spectrum to the same time exposure as the real flight data, as the latter is much smaller.
Therefore it is possible to calculate $$R$$:
$$
R = \frac {\sum_i {⌊ \frac{ni, ref \times t_{real}}{6000}⌋} \; \times \; { {|LF_i - {LF_\text{average,ref}}|^{-1/b}}}}{\sum_i {n_i,real}  \;\times\;{|LF_i - {LF_\text{average,real}}|^{-1/b}}}
$$
Where:
- $$n_{i,ref}$$ and $$n_{i,real}$$ are the number of occurrences at each load factor level $$LF_i$$ in the reference and real spectra, respectively.

- $$LF_{average}$$ is the mean load factor for the respective spectrum.

- $$b$$  is the slope of the $$S/N$$ curve.

  

$$
R = \frac {\sum_i {⌊ \frac{ni, ref \times t_{real}}{6000}⌋} \; \times \; { {|LF_i - {LF_\text{average,ref}}|^{-1/b}}}}{\sum_i {n_i,real}  \;\times\;{|LF_i - {LF_\text{average,real}}|^{-1/b}}}
$$

$$
\boxed{t_\text{extension} = t_\text{remaining \;ref} \times ( \frac {\sum_i {⌊ \frac{ni, ref \times t_{real}}{6000}⌋} \; \times \; { {|LF_i - {LF_\text{average,ref}}|^{-1/b}}}}{\sum_i {n_i,real}  \;\times\;{|LF_i - {LF_\text{average,real}}|^{-1/b}}} - 1)
}
$$



To illustrate the time extension estimation, if real damage over 25 hours is 0.000035, and reference damage is 0.0007  (i.e., $R = 20$), and the glider has 500 hours left before 12,000 hours under reference spectrum use, the extension is $$t_{\text{extension}} = 500 \times (20 - 1) = 9,500 \, \text{hours} $$.

As the following paragraphs will show, despite the variability from glider to glider, due to airframe response to turbulence, type of operations,  as well as pilot skills, the $$R$$  factor can reach a few hundred.
To ensure significant life extension is achieved, especially when glider operations result in a lower  $$R$$ value, it is recommended to start instrumentation as soon as possible. As an example, it might be wise to instrument the glider when the last 1,000-hour check is performed, before reaching the 12,000-hour limit.

However, it should be understood that the $$R$$ ratio and time extension are highly dependent on the way the glider is being flown. Gliders being flown aggressively, performing spin entry/recovery or other maneuvers requiring a wide load factor range, will have much less favorable time extension than gliders being flown cross-country with pilots flying softly.
In essence, regardless of the mission profile, gentler flying techniques will result in a greater potential life extension.



#### 3.3.3  Material parameter $$b$$

It is interesting to note that, when the reference and real spectra are given, only the parameter $$b$$ of the Basquin equation ( $$S/N$$ curve slope) has an impact on the damage and ratio calculation.
Here is a list of typical $$b$$ values used in glider constructions:

Glass Fiber Reinforced Polymer (GFRP) :

- Range for $$b$$  : -0.07 to -0.1    [15]  [16] 
- GFRP fatigue is dominated by progressive fiber-matrix debonding, matrix cracking, and fiber breakage. The lower value is driven by  fiber-matrix composites (typically epoxy) and off-axis performance.

Carbon Fiber Reinforced Polymer (CFRP) :

- Range for $$b$$  : -0.04 to -0.10  [17]  [18] 

- CFRP has a slightly better fatigue resistance due to superior carbon fiber. Like GFRP, the lower value is driven by  fiber-matrix composites (typically epoxy) and off-axis performance.



To avoid taking into account gliders' specific materials and construction, we can choose the most conservative b value for all composite materials i.e.   $$b = -0.15$$,  therefore    $$-1/b = 6.6$$. This value overestimates damage for CFRP but ensures worst-case safety for GFRP which is more often used on older gliders.

The equation for damage accumulation for the $$real$$ spectrum becomes:

$$
D_{real}\;=\;\frac{1}{C'}\sum_i {n_{i,real}} \;{\bigl|\mathrm{LF}_{i,real}-{LF_{average,real}}\bigr|^{6.6}}
$$

$$
where \;\;C' \;=\;3\;\sum_i n_{i,ref}\,\bigl|\mathrm{LF}_{i,ref}-{LF_{average,ref}}\bigr|^{6.6}
$$

As long as $$D_{real}$$ stays below  $$\frac{1}{3}$$, the glider can continue operations.



The equation for the life extension becomes:
$$
\boxed{t_\text{extension} = t_\text{remaining ref} \times ( \frac {\sum_i {⌊ \frac{ni, ref \times t_{real}}{6000}⌋} \; \times \; { {|LF_i - {LF_\text{average,ref}}|^{6.6}}}}{\sum_i {n_i,real}  \;\times\;{|LF_i - {LF_\text{average,real}}|^{6.6}}} - 1)}
$$

From a fatigue standpoint, this is a very conservative and safe approach, which provides significant safety margin.

It should be noted that the Palmgren-Miner rule and the $$S/N$$ curves are agnostic of the material being used.
We could also consider the metallic parts using a typical Basquin parameter for aluminum  $$b= -0.2$$,    $$-1/b = 5$$ ,  and apply the same calculation method to metallic parts. Contrary to composite structures, the metallic parts can be inspected, but this is important to understand how metallic parts are aging to ensure the inspection interval is appropriate. 



## 4. Results and discussion

### 4.1 Comparative occurrences analysis

Preliminary calculations performed on a Janus B glider, using approximately 35 hours of flight data in various conditions,  indicate that the real load spectrum produces significantly lower load factor occurrences than the reference model predicts. This reduction in load factor occurrences also translates into lower cumulative damage. The corresponding  damage ratio supports the potential for life extension.

The load spectrum used as a reference is the Kossira & Reinke flight-only spectrum, which excludes simple aerobatics and ground operations. This represents the most conservative choice within the available Kossira & Reinke spectra: adding simple aerobatics and ground operations would introduce additional occurrences at higher load factors, increasing the reference damage accumulation and yielding a more favorable damage ratio. The life extension results presented here therefore constitute a conservative lower bound of the potential gain.



### 4.2   Palmgren-Miner damage accumulation and  ratio evaluation

The simplified ratio:
$$
R = \frac {\sum_i {⌊ \frac{ni, ref \times t_{real}}{6000}⌋} \;\times\;{ {|LF_i - {LF_\text{average,ref}}|^{6.6}}}}{\sum_i {n_i,real}  \;\times\;{|LF_i - {LF_\text{average,real}}|^{6.6}}}
$$
provides a direct method to evaluate the difference in damage accumulation. Since real flight loads are less severe than those predicted by the Kossira & Reinke distribution, $R$ is expected to be significantly greater than one, thereby justifying an extension in the glider’s operational life.

The following is an example of  calculations performed with the conservative value of $$-1/b = 6.6$$, corresponding to worst-case GFRP structures.

A very preliminary analysis has been performed on several flights with different pilots on a Janus B.
The recording performed at 20 Hz sample rate was processed using the Kossira & Reinke counting method.

Using the Janus B data and the Kossira & Reinke reference spectrum, Table 2 provides the different steps to compute the damage ratio. Because of the limited data, this table should be considered more as an illustration of the method.



![](.\life JANUS k=6.6 v3.jpg)

​								Table 2: Palmgren-Miner ratio and life extension calculation



In this table the parameter K = $$-1/b$$ , corresponds to the slope of the $$S/N$$ curve and the Basquin parameter.

The damage ratio is simply the ratio of the $$Kossira \; occ * |n - avg|^K$$  column and $$ JANUS \; occ * |n - avg|^K$$ column sum.

where 

$$Kossira \; occ * |n - avg|^K$$ corresponds to   $${\sum_i {⌊ \frac{ni, ref\times t_{real}}{6000}⌋} \;\times\;{ {|LF_i - {LF_\text{average,ref}}|^{6.6}}}}$$

$$ JANUS \; occ * |n - avg|^K$$   corresponds to   $$\sum_i {n_i,real}  \;\times\;{|LF_i - {LF_\text{average,real}}|^{6.6}}$$



As shown in Table 2, the ratio between the Kossira & Reinke and real flight damage accumulation is 32.
Assuming the glider continues to operate with a similar load spectrum until it reaches 12,000 hours (i.e. in ~300 hours), the life extension would be around 9,300 hours ( (32-1) x 300 ).

Table 2 can also be used to help understand the sensitivity of the Palmgren-Miner ratio $$R$$ to the type of flight operations. If we imagine a pilot performing a constant 4g loop every two hours of flying, because the Table 2 data is normalized to 6,000 hours, this would add 3,000 occurrences to classes 17 to 26 and would reduce the $$R$$ ratio example from 32 down to 2.
This illustrates that the proposed method will justify life extension according to the use of the glider, and that a few high-load maneuvers will have a significant effect on the $$R$$ ratio, as per the Palmgren-Miner rule.  It should be noted that the  $$R$$ ratio of 2, due to the loops, is not accurate since the reference spectrum used for calculations is a flight-only, without aerobatics, spectrum. The purpose of the illustration is only to show that the $$R$$ ratio obtained when flying normally would be reduced by a factor of 16 due to aggressive maneuvers. 

This study focuses on composite glider parts, hence the conservative GFRP $$6.6$$ Basquin parameter. It is however interesting to note that, if a more conservative Basquin parameter, typical of aluminum alloys : $$-\frac{1}{b} = 5$$  is used, we still obtain a very significant ratio of 12. This could be used to estimate the metallic parts life extension which would be around 3,600 hours (12 x 300 ), based on the Janus data. This is significantly more than the repetitive 1,000-hour inspections, currently required after 9,000 hours. This legitimizes the continuation of these recurring inspections at 13,000 hours, 14,000 hours and beyond.
It should also be noted that, contrary to the composite structures, these metallic parts (wing shear pins and bushings, spar pins and bushings, tail fittings, etc.) can generally be inspected and eventually replaced during the repetitive inspections, reducing further the risk of failure. 



### 4.3 Practical implications, safety and certification

Using this novel Structural Life Monitoring method, it is possible to tailor a given glider's life, beyond the initially certified 12,000-hour limit, as a function of its specific usage. This life limit extension is achieved while maintaining the level of damage accumulation accepted during certification.
EASA has already accepted several methods to comply with fatigue strength regulation requirements. This legitimizes SLM as an additional alternative solution for aging gliders. 
EASA Certification Memorandum CM‑S‑006 endorses the use of the Kossira & Reinke spectra which have been designed to cover all types of usage, including some operations which are rarely performed by most gliders. While the proposed solution is consistent with these EASA reference load spectra and maintains significant calculation margins, we still anticipate a large difference between the measured and the reference damage accumulations. This  has been confirmed during initial tests on several instrumented gliders. Still, the exact extension granted by the proposed SLM method will account for actual glider use, on a serial number basis.

As the life increase is proportional to the time the real spectrum is observed, it is advisable to instrument gliders as soon as possible and before they reach 12,000 hours, to be able to gain significant life extension.
Early life instrumentation might not be necessary when solely considering aging glider life extension, but would provide valuable data and statistics on glider usage. 

#### 4.3.1  Concept of Operation and Deployment Proposals

##### 4.3.1.1 Concept of Operation Proposal

The concept of operation could be divided into 3 main phases:

###### Phase 1 — Instrumentation and Data Collection (below Type Certificate safe life limit)

This phase covers the period during which the SLM recorder is installed, and the glider has not yet reached its safe life limit. It includes:
\-    Sensor installation in accordance with CS-STAN / Form 123
\-    Annual 6-face calibration during the annual inspection
\-    Compliance with Part ML; installation and annual calibration results recorded in the aircraft logbook
\-    Missing data policy: if a flight occurs without valid SLM data (sensor fault, data corruption, missed calibration), damage for that flight is substituted at the reference Kossira & Reinke damage rate for the flight duration
\-    Flight data uploaded to the central web repository; post-processing tools applied to guarantee data integrity

###### Phase 2 — Fatigue Evaluation when reaching Type Certificate safe life limit

This phase includes:
\-    a dedicated fatigue inspection of the aircraft condition (equivalent in scope to the existing recurring 1,000-hour inspections).
\-    an assessment of the real cumulative damage to possibly permit operation up to the originally certified fatigue damage limit.
\-    inspection beyond the composite structure, as well as an overall assessment of the glider’s condition (incidents/repairs). 

######  Phase 3 — Operation Beyond Type Certificate safe life limit

 This phase is a continuation of Phase 1 monitoring operations, with the following additional provisions:
\-    Go / No-Go decision at each Airworthiness Review Certificate (ARC) renewal, based on the SLM fatigue status report
\-    Go criterion: cumulative D_total < 1/3, AND the current damage rate (D per flight hour) confirms that D = 1/3 will not be reached before the next scheduled inspection
\-    Recurring structural inspection continuing from Phase 2, with a maximum interval of 1,000 hours or 5 years, whichever is sooner
\-    This process continues until the aircraft has exhausted its remaining damage potential and is retired from service



##### 4.3.1.2 Validation of the concept and Deployment proposal

The SLM solution has never been implemented on gliders and there is no Interpretative Material (IM) or Acceptable Means of Compliance (AMC) to support CS-22 certification.
One important step toward SLM approval will be the publication of a Certification Review Item, which shall support the establishment of IM or AMC.
The CRI shall cover acceptable:
 \- fatigue/damage calculation methods
 \- reference load spectrum and composite material parameter
 \- onboard recording solution
 \- postprocessing solution
 \- CONOPS and Instructions for Continued Airworthiness (including impact on AFM/AMM/AMP)
 \- limits of proposed methodology  and SLM applicability

An EASA STC could be used to develop the required certification justification documents.
The STC could be applicable to a small group of gliders in experimentation. They would provide flight data as well as validate the CONOPS.
The STC would produce the following documents which will be required to get the SLM approved:

- Certification Program
- Certification Review Item
- Methodology Report
- Instructions for Continued Airworthiness
- Installation, Operating and Maintenance Manual

Once the STC is approved, the gliders in experimentation would be allowed to continue their operation using SLM.
The STC documents could be made available to the interested Type Certificate holders. They could develop modifications and Service Bulletins to permit SLM operation on selected glider types.



## 5. Conclusion

This paper presents a methodology for extending the operational life of composite gliders using Structural Life Monitoring. By measuring in-flight accelerations and processing them with the Palmgren-Miner rule, it is possible to compute a glider's real cumulative fatigue damage. Crucially, both the reference and real flight spectra are processed using the same Kossira & Reinke counting method, ensuring a consistent and legitimate comparison. As long as real cumulative damage does not exceed the certification damage limit established during type certification, continued operation is justified — without any requirement to reopen Type Certificate documents or revise certified structural limits.

Preliminary results show that, even when applying conservative calculation methods and worst-case composite material fatigue parameters, damage accumulation from actual flights is orders of magnitude lower than damage accumulation predicted by the reference spectrum. A damage ratio of around 30 has been observed on an instrumented glider, corresponding to potential life extensions of several thousand hours for typical training and cross-country operations. Interestingly, the same approach applied to metallic components, using aluminum Basquin parameters, also yields significant life extension, legitimizing the continuation of recurring structural inspections beyond the current life limit. It should however be noted that life extension is directly dependent on how the glider is flown — gentler flying results in proportionally greater extension.

These findings are consistent with life assessments performed on similar composite structures in other industries, and with the 65,000-hour life assessment performed by TRAFI for the PIK-20D in 2015.

The proposed method is conservative by design, compatible with EASA fatigue strength regulation requirements, and provides economic and environmental benefits while maintaining the same safety level as the original Type Certificate (same certified damage limit as the original TC). A structured three-phase Concept of Operation — covering instrumentation, fatigue evaluation at the certified life limit, and monitored operation beyond it — has been outlined as a practical deployment framework. It is advisable to first validate this approach on a selected fleet of instrumented gliders. The findings could then support the establishment of an EASA Certification Review Item, leading to an Acceptable Means of Compliance for SLM under CS-22, and ultimately deployed on aging gliders through Supplemental Type Certificates or manufacturer Service Bulletins.



## References

1. Kossira, H. and Reinke, W. (OSTIV Publication XVI). “Determination of load spectra for the design of sailplanes.”

2. Kossira, H. (1982). “Determination of load spectra and their application for keeping the operational life proof of sporting airplanes.” *ICAS-Proc. 8/1982; ICAS-82-2.8.2*, pp. 1330-1338.

3. EASA Certification Memorandum CM‑S‑006, *Certification, Type Design Definition, Material and Process Qualification for Composite Light Aircraft*. [Available at: [EASA Document Library](https://www.easa.europa.eu/en/document-library/product-certification-consultations/easa-cm-s-006)]

4. Pommera, G. (2000). *Minutes of LBA/DGAC meeting dedicated to 12,000 hours gliders fatigue life – November 14, 2000*.

5. LBA Document, *German LBA Standards for Structural Substantiation – Master*.

6. Easy Access Rules for Very Light Aeroplanes (CS-VLA)  /  EASA AMC VLA 572

7.  Kensche, C. (2019). Numerical Comparison of Glider Load Spectra. Technical Soaring.

8.  Soinne , Erkki (2015), PIK-20D Fatigue evaluation, Trafi Research Reports Trafin tutkimuksia Trafis undersökningsrapporter 7/2015

9.  C.A. Patching & L.A. Wood (1991). Fatigue testing of a GFRP glider, OSTIV Congress, Uvalde, Texas, U.S.A.

10. Standard practices for cycle counting in fatigue analysis. ASTM E 1049-85.

11. Kossira H., Reinke W., Festigkeit von modernen GFK-Konstruktionen für Segelflugzeuge - Bestimmung eines Belastungskollektives, IFL-IB 84-01 Technische Universität Braunschweig.

12. Miner, M. A. (1945). *Cumulative Damage in Fatigue.* Journal of the Engineering Mechanics Division.

13. Palmgren, A. (1947). *A Probabilistic Theory of Cumulative Damage.*

14. Basquin, O.H. (1910).  "The exponential law of endurance tests." Proceedings of the ASTM, Vol. 10, pp. 625–630.

15. Mandell, J. F. (1982). *Fatigue Behavior of Fiber Resin Composites*. Elsevier.

16. Harris, B. (2003). *Fatigue in Composites: Science and Technology of the Fatigue Response of Fibre-Reinforced Plastics*. Woodhead Publishing.

17. Talreja, R. (1985). *Fatigue of Composite Materials*. Technomic Publishing.

18. Bathias, C. (1999). *Fatigue of Materials and Structures: Application to Design and Damage*. Wiley.

    