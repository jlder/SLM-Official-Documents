

# 		    			Extension of Glider Life using

#  	    					Structural Life Monitoring



​								by   Jean-Luc Derouineau,
​				*Fédération Française de Vol en Planeur   /   European Gliding Union*



[toc]



## Abstract

The lifespan of a glider, like any structure, is limited by its inherent susceptibility to fatigue damage. Similar to other structures, the repeated application of cyclic stress or load can cause the accumulation of damage, ultimately leading to delamination and the formation of cracks and dictating its useful operational duration.

To mitigate potential risks associated with fatigue on composite gliders, the EASA (European Union Aviation Safety Agency) accepts at least two methods to demonstrate compliance to life requirements. These acceptable means of compliance (AMC) are either a traditional fatigue analysis, and its corresponding lengthy and costly tests, or a simpler overload test of the glider, at the ultimate load level plus a certain margin. In either case, the applicant is currently granted a 12,000-hour life limit by the EASA. However, it is noteworthy that both means of compliance go beyond CS 22.627 fatigue strength regulation requirement.

The 12,000-hour life limit imposes a financial burden on glider clubs, which are not able to afford more recent used or new gliders. From an environmental standpoint, there are currently no solutions to recycling composite gliders when they reach end of life. Any opportunity to extend glider life would be instrumental for the glider community and the environment. 

This paper presents a method, consistent with modern Structural Health Monitoring solutions, using Structural Life Monitoring (SLM) to justify increased fatigue life. The method analyzes the differences between reference load spectrum, recognized by EASA for life prediction,  and the actual load spectrum, experienced during real flights. 

Damages accumulate on the glider structure as function of the load factor cycle occurrences. Load spectra are representations of these occurrences expressed as function of load factors. Using the Miner-Palmgren rule, it is possible to estimate the cumulative damages of the corresponding spectra.  The damage accumulation, calculated with the reference load spectrum at 12,000 hours, sets the limit of damage that should not be exceeded. A glider can therefore operate until this limit is reached. If the rate of damage accumulation from real flights is lower than the theoretical rate of damage accumulation, the glider should be able to fly beyond 12,000 hours, until the certification damage limit is reached. It is important to note that with SLM, the structural limits validated during initial glider certification do not need to be revisited and increased, there is no requirement to reopen certification structural justification documents.

This approach is consistent with EASA recommendations, which acknowledge multiple methods can be used for life justification due to fatigue, and is proposing SLM as an additional Means of Compliance (MoC).

The reference load spectra are from Kossira & Reinke work. They have established multiple spectra based on real flights experience.
The real flights load spectrum is computed with the same Kossira & Reinke counting method, using the accelerations measured on the glider. 
Because the reference load factor spectrum shall cover the envelope of all possible glider usages, it is by design conservative compared to the real flight spectrum. Differences of orders of magnitude are expected between the damage calculations. For typical training and cross-country flying, this method can potentially  extend a glider's life by thousands of hours, significantly increasing  its value and reducing its environmental footprint.



## Acknowledgements

The development of this white paper benefited significantly from the input and support provided by multiple reviewers, representing considerable expertise in the domain of glider structure, fatigue, flight dynamics and analytics.
I would like to give special thanks to each of them for sharing their time and expertise.
Reviewers: (in alphabetical order)
Kensche Christoph, Mesnil Guy François, Regis Olivier, Radespiel Rolf, Scherrer Matthieu, Scholz Werner.



## 1. Introduction

Prediction of aircraft life is critical for ensuring safety and cost-value efficiency:

- Cost is affected by life because of design solutions, material selection, and associated manufacturing. 
- Value is affected by life since used gliders depreciate suddenly when reaching their end of life. 

This is becoming a costly dilemma for small glider clubs which may not be able to replace their old gliders with more recent new or used models.
The carbon footprint of composite structures is also a growing environmental concern since glider manufacturers currently do not provide solutions for recycling their composite gliders.
Extending glider life would extend their value and reduce the environmental impact.

Traditionally, glider life prediction methods have relied on standardized theoretical load spectra, such as those developed by Kossira & Reinke [1]. The load spectra, derived from these seminal works [2], have become a key reference in defining load expectations for sailplane design and certification (EASA CS-22). These spectra were established using a compilation of a few hundred hours of real flights measurements performed on several gliders, flying in multiple conditions. The data and corresponding load factor occurrences have been extrapolated, using predefined operational profiles, to cover the envelope of all possible glider usages.

Recommendations by the European Union Aviation Safety Agency (EASA), as detailed in Certification Memorandum CM‑S‑006 [3], advocate for the use of these spectra for fatigue testing and structural analysis. In particular, the KoSMOS spectrum, which  is the most recent version, created to reduce testing time when actual laboratory fatigue tests are performed. 

EASA and other authorities have accepted several acceptable methods for compliance to fatigue strength regulation requirement (CS 22.627), including full scale fatigue testing based on accepted theoretical spectrum as well as static load tests with additional required safety margins [4] (5) [6].

The granted 12,000-hour life limit, using either previously described solutions, sets the level of maximum acceptable damage accumulation. Attempts have been made in the past, using modern modeling tools and recently available material fatigue data, to quantify and justify that the composite structures  have much lower damage accumulation rate compared to what was expected during initial certification [7]. However, because it is impractical to re-open 50 years old certification documents, the proposed solution is using structural Health Monitoring principles, to demonstrate that there are opportunities to justify operations beyond 12,000 hours, without exceeding the maximum acceptable damage accumulation set during initial certification, eliminating the need to reopen Type Certificate (TC) documents.
The real damage accumulation is computed using inflight acceleration measurements, with the Miner-Palmgren rule. The number of cycles to failure, required for damage calculation, is computed using the reference cycle, the composite material properties and the certification damage limit. The principle is shown on Figure 1.

![](C:\Users\JLD\Downloads\12000\life extesion graphic v1.jpg)

​						Figure 1: Life extension principle



## 2. Background and literature review

### 2.1 State Of the Art

#### 2.1.1 Introduction of life limit in glider industry

Until the introduction of composite materials, gliders were manufactured using wood, fabric and aluminum. The fatigue behavior of these materials is well understood, only requiring standard practice to avoid any concentration of stress above certification limits. At the time of certification of the older gliders, it is assumed that no explicit fatigue life analysis or testing was required.
The first composite gliders were manufactured in the late 1950s: fs 24 Phönix first flight was in 1957, followed by Hütter H 30 GFK in 1962 (which led to the Glasflügel Libelle) and Akaflieg Darmstadt D-36 in 1964. The D-36 led to the ASW 12 (Waibel / Schleicher), the Cirrus (Holighaus / Schempp-Hirth) and LS1 (Lemke / LS) sailplanes which were then built in series. By the 1970s, composite materials became the standard in high-performance glider manufacturing, and all modern gliders today are made with advanced composite structures.

The glider community has been a pioneer in the use of composite materials, but industry's relative inexperience and limited understanding of fatigue behavior, led some certification authorities to introduce a life limit. This 12,000-hour limit, which was set by LBA (Luftfahrt-Bundesamt), remains the standard life limit today under EASA.
It should be noted that, even if authorities like LBA imposed a relatively short limit to new designs, other authorities such as TRAFI [8]  (Finland) and DGAC (France) approved much higher limits or even no limit (PIK20, Centrair C101).

#### 2.1.2 Current state and possible evolutions

Today, the EASA has maintained the 12,000-hour life limit, although the CS 22.627 (Fatigue strength) only requires that "structure must be designed, as far as practicable, to avoid points of stress concentration where variable stresses above the fatigue limit are likely to occur in normal service".

In the glider industry, there have been few full-scale fatigue testing performed. In most cases, the glider manufacturers have been complying with the requirement using the EASA accepted static overload test.
However, there has been one particularly interesting full scale fatigue test performed in the 1990s, in Australia, on a Janus B wing [9]. The glider was not new and one wing had substantial repairs. Some defects were not repaired on purpose and some defects were created to simulate typical incidents (such as wing damage during out-landing). The conclusion was clear confirming that there were no significant damage accumulation on the wing without repair and, only the non-repaired  sections had substantial growth of  minor unrepaired damages. However, the propagation rate of delamination was slow and could be easily detected with the 1000-hour inspection interval.

The experience gained in aerospace industry, as well as other industries like wind turbines, from inspection of aging composite structures, improved fiber characterization and better modeling, has validated the excellent fatigue behavior of composite airframes. This confirms that the historical 12,000-hour life limit imposed to gliders is extremely conservative as already demonstrated in previous analysis "Numerical Comparison of Glider Load Spectra" [7].

Even if recent analysis have identified structural margin opportunities, it is not practical to reopen structure analysis for gliders certified 30 or more years ago. However, thanks to better understanding of glider operational usage and the corresponding composite materials damage accumulation due to fatigue, our proposed method provides a solution to extend the life of gliders, without changing the certification damage accumulation limit associated to 12,000 hours.



### 2.2 Reference load spectrum, distribution occurrences and application to operational life assessment

The load spectra developed by Kossira & Reinke are foundational in sailplane design. In their seminal work, *“Determination of load spectra for the design of sailplanes”* [1], they established a methodology for deriving a reference or theoretical load spectrum that includes both the stress levels and the occurrence frequency (distribution) of these load events.
To establish their load spectra, they instrumented gliders which were flown in different conditions, with the goal of being representative of the envelope of all possible flight usages. Because they could only fly for a limited time, it was necessary to scale the data to be representative of 6,000 or 12,000 flight hours required for certification. They used an extrapolation method which not only scales the occurrences as function of time, but also increases the maximum and minimum load cycles values. While this extrapolation method is understandable, from a statistical point of view to account for the lack of variability due to reduced flight time, it might be a source of over-estimation.

The counting method used by Kossira & Reinke is very similar to the "peak and valley" solution [10], with the addition of a simple filter to avoid counting minor load factor variations, and the eventual use of Markov matrix transition to count occurrences. These occurrences specify the expected number of cycles at various stress levels over a defined operational period, and form the basis for fatigue life predictions. However, we should understand that these spectra have been developed to cover the envelope of all possible operations and have built-in conservatism compared to most typical operations.
Because the KoSMOS spectra (Kollektiv für Segelflugzeuge, Motorflugzeuge und Motor-Segler, i.e. load collective for sailplanes, aeroplanes and powered gliders) and the associated Markov matrix are not readily available in the public domain,  the initial study has been performed using the original Kossira & Reinke spectra from their 1982 publication [2]. This choice could be revisited while experimenting with additional gliders, to make the life extension estimations  more in line with the certification hypothesis.

Figure 2 is a representation of the Kossira & Reinke flight only spectrum normalized at 6000 flight hours. This spectrum only includes flight phases without any aerobatics, making it conservative (fewer occurrences at reduced load factors)

![](C:\Users\JLD\Downloads\12000\Kossira spectra flight only 6000FH v1.jpg)

​				Figure 2: Kossira & Reinke spectrum normalized for 6000 Flight Hours [2]
​							 (x axis: occurrences /  y axis: load factor)

Kossira & Reinke’s subsequent work, *“Determination of load spectra and their application for keeping the operational life proof of sporting airplanes”* [2], extends these concepts to operational life assessment. The occurrence distribution, in this framework, enables the calculation of cumulative damage via cycle counts.



### 2.3 Kossira & Reinke counting method

Multiple counting methods have been developed over time, e.g. level crossing, peaks & valleys or Rainflow [10], and there are differences in the resulting occurrence calculations. The goal of this study is to compare the damage accumulation between the theoretical  spectrum and real flights spectra, and use the counting method developed by Kossira & Reinke [2] for their own spectra to compute occurrences for the real flights spectra.

#### 2.3.1 Kossira & Reinke counting method principle

The Kossira & Reinke spectra were developed in the eighties to provide glider designers with load spectra which could be used for fatigue analysis, tests, and life justifications [2].

These spectra  are referenced by EASA in their certification memorandum (CM-S-006 Issue 01 issued 20 January 2015) [3].

To establish these spectra, gliders have been instrumented to record stress on wing during multiple phases of flight. 
Using limited digital technology available at that time, the acquisition and processing were relatively simple: 

1. Converting the wing loading, calculated with the spar bending moments divided by a reference bending moment, into digital classes of 2<sup>10</sup> and  2<sup>5</sup> precision, 
2. simple filtering to reduce the effect of small load factor variations,
3. identifying maxima and minima in the smaller  2<sup>5</sup> class (maxima and minima are also called peaks & valleys), 
4. filling a Markov transition matrix using "from stress/load factor"  to "to stress/load factor" transitions which correspond to transitions from minimum (valley) to maximum (peak) as well as  maximum (peak) to minimum (valley),
5. transforming the Markov matrix to count exceedances above and below the average load factor level,
6. summing the cells of the lines of the transformed Markov matrix to create the more user friendly Load Factor as function of occurrences exceedances graphic.

This final step provides the representation in Figure 2 and Figure 3 which are commonly called load spectra and which can be used for damage and life analysis. It is interesting to note that, while the values are slightly different, the shape and the average values between the theoretical and real spectra are consistent. 



<img src=".\spectrum_ventus.jpg" style="zoom: 67%;" />

​			Figure 3: Examples of Kossira & Reinke flight only spectrum and real flights Ventus spectrum
​								 ( x axis: occurrences /  y axis: load factor)



#### 2.3.2 Acquisition and classes

The sensor's signal, representing the glider body vertical axis load factor, is converted to digital values using  2<sup>10</sup> precision (signal is quantified into 1024 classes). With a typical load factor range of -4g to +6g, the differences between two adjacent classes is small (approximately 0.01g). Analyzing the transitions using this accuracy results in a high number of small transitions, which have no real value for fatigue and life analysis.
The solution proposed by Kossira & Reinke is to use a sub class using 2<sup>5</sup> precision ( signal quantified in 32 classes). With such resolution, the difference between two 32 class adjacent values is approximately 0.32g which is more representative for fatigue and life analysis.

<img src="C:\Users\JLD\Downloads\12000\class_32_1_to_32_-4_to_6.jpg" style="zoom:80%;" />

​											Table 1: Class 32 definition



#### 2.3.3 Filtering

Using data in the 32 class format is simple but has a negative effect since it amplifies small signal variations when these variations occur at the limit of the 32 class transitions. For example, with an input range of -4g to +6g,  if the value of the input signal is 0.95g, the 1024 class value is 507 and the 32 class value is 16. If the signal increases slightly by e.g. 0.08g, the 1024 class value becomes 516 and the 32 class value 17. If the input signal oscillates between these values, the class 32 values also oscillate between 16 and 17, which means that a small 0.08g input signal variation is turned into a large 0.32g variation when converted to 32 class. To avoid these undesired 32 class variations induced by small input signal variations, Kossira & Reinke introduced a simple filtering solution by only taking into account a new sample, if the difference between this new sample and the last recorded sample exceeds a threshold DX, in the 1024 class.  In their experimentations, Kossira & Reinke have used DX=10 [11], which means that the difference between previous sample and current sample has to be at least ~0.1g , for current sample to be processed. Figure 4 provides an illustration of the filtering/hysteresis proposed by Kossira & Reinke [2].

![](C:\Users\JLD\Downloads\12000\class 1024 32  filter v1.jpg)

​									Figure 4: Kossira & Reinke filtering solution



#### 2.3.4 Maxima and minima (peaks and valleys)

When the input data is filtered and reduced to the 32 class, it is straightforward to identify the minima and maxima in the data stream. The resulting data stream is a succession of minima and maxima in alternance, also called peaks and valleys, as shown on Figure 5.

<img src=".\peaksandvalleys.jpg" style="zoom:80%;" />

​							Figure 5: Maxima & Minima  /  Peaks & Valleys



#### 2.3.5 Markov transition matrix

The peaks and valleys data stream obtained from the previous steps is used to fill the Markov transition matrix, because the data is in 32 class, the matrix size is 32 x 32. The columns of the matrix correspond to the "from" load factor of a transition and the lines of the matrix correspond to the "to" load factor of the transition. The peaks and valleys are processed by taking two consecutive values which respectively correspond to the "from" load factor and the "to" load factor. The corresponding cell of the Markov transition matrix is incremented. Figure 6 provides an example of a Markov matrix from a single flight.

<img src=".\Markov1.jpg" style="zoom: 67%;" />

​							Figure 6: Example of Markov transition matrix
​					( x axis: "**from**" level transition /  y axis: "**to**" level transition )



#### 2.3.6 Load factor as function of occurrences spectrum representation

To convert the Markov transition matrix data to the more traditional load factor as function of occurrences spectrum representation, it is necessary to first determine the average load factor value for the considered flight sequence(s).
Then compute how many transitions went through a given load factor above and below the mean value:

1. for each of the load factor cells above the mean value and above diagonal, compute the sum of all the occurrences at and above the considered cell (Figure 7 red/black example)

2. for each of the load factor cells below the mean value and below diagonal, compute the sum of all the occurrences at and below the considered cell (Figure 7 green/light gray example).

   ​									![](.\Markov1to2.jpg)

​					Figure 7: Calculation of the number of transitions through a given cell
​						( x axis: "**from**" level transition /  y axis: "**to**" level transition )



For a given load factor level, sum all the occurrences to obtain the spectrum table and graphic representation, as seen on Figure 8 and Figure 9.

<img src=".\Markov2toSpectrum.jpg" style="zoom:67%;" />

​			Figure 8: Calculation of the total number of occurrences for every load factor level
​				( Left  =  x axis: "**from**" level transition /  y axis: "**to**" level transition
  				Right = x axis: number of occurrences / y axis: load factor )



![](C:\Users\JLD\Downloads\12000\Janus 6000 FH.jpg)

​					Figure 9: Example of load factor spectrum from a glider real flights in green/black 
​	with Kossira & Reinke theoretical flight only (no aerobatics) spectrum in red/gray normalized at 6000 flight hours
​							(horizontal axis: occurrences  /  vertical axis: g load)



### 2.4 Real load spectrum in glider operations

In actual glider operations, load conditions deviate from the conservative assumptions of theoretical models. Factors such as pilot technique, environmental variations, and operational profiles, lead to a real load spectrum that often exhibits fewer or less severe load events than those predicted by the Kossira & Reinke distribution. The accelerations measured during actual flights are processed using Kossira & Reinke counting method to provide these real load spectra.



### 2.5 Fatigue damage accumulation: the Miner-Palmgren rule

Since the spectra have been established with the same counting method, it is reasonable to use the same solution to estimate and compare the fatigue or damage corresponding to each spectrum.
The Miner-Palmgren rule [12] [13] provides a linear damage accumulation model for fatigue, expressed as:
$$
D = \sum_i \frac{n_i}{N_i} 
$$
where $n_i$ is the number of cycles at a specific stress level, and $N_i$ is the number of cycles to failure at that level. When $$D$$ reaches the value 1, the structure is considered to have failed.
In sailplane fatigue context, damage accumulation $$D$$ corresponds to the sum of individual damages computed at each considered load factor level (stress level), either in operation (real load spectrum) or using theoretical spectrum. Each individual damage, at a given stress level, is the ratio between the occurrences applied to the structure at that level ($$n_i$$) and the number of occurrences required to fail the structure at that same stress level ($$N_i$$). 

It is therefore possible to estimate damage accumulation from a given spectrum to ensure the value stays below a certain limit.
When multiple spectra are available,  and the respective damage accumulations are estimated over the same exposure time, it becomes possible to compare to estimate life extension.



### 2.6 Number of cycles to failure ($$N_i$$)

For a given load spectrum, either theoretical or from actual flight measurements, the occurrences at a given stress level $$n_i$$  are known. To estimate the damage accumulation $$D$$, corresponding to that spectrum, we only need $$N_i$$, which is the number of occurrences required to fail the structure at each load factor/stress level.

#### 2.6.1 Material fatigue representation - $$S/N curve$$

Modeling fatigue is instrumental to understanding how materials  behave under occurrences of loading. This is vital for industries such as  aerospace, automotive, and construction. One  tool used to represent fatigue data is the **S-N curve**, originally known as the Wöhler curve. 

Wöhler's work has been at the root of modern fatigue analysis and testing. It introduced the first graphical representation of stress vs. cycles to failure and is now commonly referred to as the S-N curve as pictured on Figure 10.

An S-N curve provides a representation of the relationship between the stress amplitude (**S**) applied to a material and the number of cycles to failure (**N**) it can endure. 

- $$S\;:$$ Stress a material experiences during a single cycle.
- $$N\;:$$ Total number of cycles a material can withstand before failing.

For fatigue analysis and demonstrations, there is a direct correlation between stress cycles and load factor cycles due to the stress considered: structure flection under load factor. 

<img src="C:\Users\JLD\Downloads\12000\SN_curve simple v1.png" style="zoom:67%;" />

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

With the exception of $$N$$, all material properties parameters are constants.
For this purpose, the Basquin equation simplifies to:
$$
\sigma_{a} \;=\; C \; N^{b}
$$
with $$C$$ constant : 
$$
C\; = \sigma'_f\;\Bigl(\frac{2}{\varepsilon'_F}\Bigr)^{b}
$$
It expresses the stress‐amplitude $σ_a$ required to produce failure in $N$ cycles as a power‑law function of $N$.

This model is only valid for the high cycle fatigue of the $$S/N$$ curve, and is not an issue for this application as, by design margins, a glider does not operate into the low cycle fatigue and, at the other end of the curve, it is known that very low amplitude stress occurrences do not contribute to fatigue and can be ignored.



#### 2.6.3 End of life damage accumulation estimation

By design and construction, a glider has a life potential for damage due to cycle fatigue.
While the glider is in use, this potential is consumed by the occurrence of the load variations (cycles).
The theoretical load factor spectrum and the real load factor spectrum are two examples of how the occurrences are distributed as function of the load factor as well as their frequency.
When the potential is consumed, the component(s) subject to fatigue could fail. When the Miner-Palmgren rule is used as a way to estimate damage accumulation, this means the corresponding value  $$D$$ has reached $$1$$.

Certification requirements and common practice incorporate a safety factor of 3, so that if a life of e.g., 12,000 hours is targeted, the calculations and validations should be performed for a duration of 36,000 hours.

Therefore when using Kossira & Reinke as the reference theoretical spectrum, and Miner-Palmgren as a way to estimate damage, the damage accumulation is:
$$
D_{theoretical,36000}\;=\;\sum_i \frac{n_{i,theoretical,36000}}{N_i}\; = 1
$$
when the spectrum of occurrences corresponds to 36000 hours exposure time,
and:
$$
D_{theoretical,12000}\;=\;\sum_i \frac{n_{i,theoretical,12000}}{N_i}\; = \frac{1}{3}
$$
when spectrum of occurrences corresponds to 12,000-hour exposure time.

$$
\boxed{D = \frac {1}{3}}
$$
This damage value corresponds to 12,000-hour life potential limit for damage accumulation.



#### 2.6.4 Estimation of the number of cycles to failure $${N_i}$$

Local stresses can be considered linear with the load factor around average load factor:
$$
σ_{a,i} \;\propto\;|LF_i - {LF_\text{average}}\bigr|
$$
with  $${LF_i}$$  the load factor and $${LF_\text{average}}$$  the average load factor during the exposed time.
Using the Basquin model, with a constant $$C'$$ which can be derived from the certification condition using the theoretical spectrum:
$$
|LF_i - {LF_\text{average}}\bigr|\propto\  C'\,N_i^b
$$

$$
N_i \;=\; C'\;\bigl|LF_i - {LF_\text{average}}\bigr|^{1/b}
$$

with $C'$ being a proportionality constant which can be calculated using the defined theoretical damage accumulation: 

$$
D_{theoretical,12000}\;=\;\sum_i \frac{n_{i,theoretical,12000}}{N_i}\; = \frac{1}{3}
$$


$$
with  \; N_i \;=\; C'\;\bigl|\mathrm{LF}_i - {LF_{average}}\bigr|^{1/b}
$$

$$
\sum_i \frac{n_{i,theoretical,12000}}{N_i} = \frac{1}{3}
\quad\Longrightarrow\quad
\sum_i \frac{n_{i,theoretical,12000}}{\,C'\bigl|LF_i - {LF_\text{average}}\bigr|^{1/b}\,} = \frac{1}{3}.
$$

$$
\sum_i \frac{n_{i,theoretical,12000}\,|\mathrm{LF}_i-{LF_{average}}|^{-1/b}}{C'} \;=\;\frac {1}{3}.
$$

$$
\frac{1}{C'}\,\sum_i n_{i,theoretical,12000}\,\bigl|\mathrm{LF}_i-{LF_{average}}\bigr|^{-1/b} \;=\;\frac{1}{3}
$$

$$
\quad\Longrightarrow\quad
C' \;=\;3\;\sum_i n_{i,theoretical,12000}\,\bigl|\mathrm{LF}_i-{LF_{average}}\bigr|^{-1/b}.
$$

The complete expression to calculate the $$N_i$$ values which can be used to assess cumulative damage can be written as:
$$
\boxed{%
N_i \;=\; \underbrace{3 \;\sum_j n_{j,theoretical,12000}\,\bigl|\mathrm{LF}_j-{LF_{average}}\bigr|^{-1/b}}_{C'}\;\bigl|\mathrm{LF}_i-{LF_{average}}\bigr|^{1/b}\,.%
}
$$
For a given spectrum $$n, \;LF \;and \;LF_{average}$$ are known, allowing to calculate $$C'$$ and subsequently all the  $$N_i$$ values for each load factor of the spectrum.
These $$N_i$$ values are only functions of the spectrum and the slope of the $$S/N$$ curve  $$b$$, as the Kossira & Reinke reference spectrum is known. If a conservative $$S/N$$ slope $$b$$ value is chosen to cover all types of composite glider structures, the resulting $$N_i$$ values would become a reference usable for all damage estimations.



## 3. Methodology

### 3.1 Data acquisition

#### 3.1.1 Acquisition of load cycle using accelerometer and strain gauges

To establish their spectra, Kossira & Reinke have been initially using strain gauges, installed on the spar, at the wing root of the glider. Their goal was to measure the bending moment $$M_{br}$$, at the wing root . To calibrate their measurement system, they loaded the wing on the ground with different weight to be representative of the lift range. Then they flew in calm air with a stable trajectory (vertical acceleration ~ 1g) to establish the reference bending moment $$M_{br1g}$$. The bending moments measured during the flights were then divided  by the reference bending moment, resulting in the ratio \(\frac{M_{br}}{M_{br1g}}\), which represents the wing loading in flight.
When the glider is mainly subject to aerodynamic forces , this $$\frac{M_{br}}{M_{br1g}}$$ ratio also represents the vertical load factor  $$N_z$$ , which can also be measured by accelerometers.
When the glider is subject to other forces, the relation $$\frac{M_{br}}{M_{br1g}}$$ = $$N_z$$ is not always true. However, if these phases can be identified and processed independently from the flight phases, flight physics models could be used to shift the accelerometer reading in order to be representative of the specific spar flexion/strain during these phases.
For example, there would be value in studying the ground rolling phases, when the wing lift is nonexistent as well as the winch takeoffs when there is significant wing lift or flexion. Until such studies are performed, it is always possible to use a “fixed fee”, added to the real fatigue spectrum, based on the same hypothesis Kossira & Reinke have used for ground maneuvers and winch launching.  As an illustration of possible simple models, in the specific case of ground rolls, the accelerometer reading could be shifted to represent the specific spar flexion/strain mean value when wing lift is non-existent (negative shift).

#### 3.1.2 Data acquisition for experimentation

Real flight load factor $$N_z$$ is recorded in real time using accelerometers  located on the wing spar, and electronic memory (e.g. SD card). The accelerometer location is critical in order to avoid acceleration noise due to centripetal accelerations when the glider attitude changes. The recommended location being on the wing spar as close as possible to the center line. 
This data is processed using the Kossira & Reinke method to build the real flights load spectra. Using the same method used by Kossira & Reinke for their theoretical spectra is important to make comparison between real and theoretical spectra legitimate.

During the initial experimentation, the takeoff and landing roll are treated as normal flight sequences. This is conservative since the typical positive Nz peaks encountered during touchdown, are accounted at a higher value than it should be, as no offset/shift is applied to the accelerometer reading. No winch takeoffs are being planned with the experimentation gliders but, if this was the case, the same Kossira & Reinke assumptions would be used to add the corresponding load cycles occurrences to the experimentation glider spectrum. This is believed to cover for the limitations of using accelerometer instead of strain gages.

Since most of the energy from turbulence or glider movement is below 10 Hz, the accelerometers should be filtered with a cutoff of at least 10 Hz, requiring a minimum sampling rate of 20 Hz. Accelerometer calibration should be checked before every flight when the glider is static to make sure the magnitude of the gravity measured on the 3 axes is ~1g.




### 3.2 Load spectrum analysis

Two load spectra are defined:

- **Reference Load Spectrum:** Based on Kossira & Reinke  (as recommended by the European Union Aviation Safety Agency), this theoretical spectrum includes the stress levels  (load factor) and their corresponding distribution occurrences (Figure 2).
- **Real Load Spectrum:** Derived from flight data, representing the actual occurrences of various stress levels during operations. To be consistent with the theoretical spectrum used as a reference, the Kossira & Reinke counting method (§ 2.4) shall be used.
  Within the scope of the initial experimentation, all phases of flight were included (takeoff, flight and landing). 

To allow comparison between spectra,  the same load factor range should be used, and the respective cycle counts $n_i$ should be normalized to the same flight duration.




### 3.3 Application of the Miner-Palmgren rule to estimate life extension

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
where \;\;C' \;=\;3\;\sum_i n_{i,theoretical,12000}\,\bigl|\mathrm{LF}_{i}-{LF_{average,theo}}\bigr|^{-1/b}
$$

As long as $$D_{real}$$ stays below  $$\frac{1}{3}$$, the glider can continue operations.

In reality, gliders will only be instrumented late in their life. The damage accumulation will be a combination of  theoretical damage (when the glider is not instrumented) and real damage (when the glider is instrumented):  
$$
D_{total} = D_{glider \; not \;instrumented} + D_{glider \; instrumented}
$$
where $$D_{glider  \; not \; instrumented}$$  is computed using the theoretical spectrum normalized for a duration equal to the time during which the  glider was flying without instrumentation.
and where $$D_{glider \; instrumented}\;=\;D_{real}$$  is computed using the real flights occurrences. There is no need to normalize as it corresponds to  the duration when the glider was instrumented.
The condition being, the glider can stay in operation as long as $$D_{total}$$ stays below  $$\frac {1}{3}$$ . 



#### 3.3.2  Life extension estimation

Once the damage from actual flights has been computed using the Miner–Palmgren rule, it is possible to estimate how much longer a glider can operate beyond the certified 12,000-hour life limit, with the important assumption that the real usage continues with the same load pattern as the flights already performed.

##### 3.3.2.1 Damage accumulation rate

As damage accumulation is assumed to be linear with respect to time under a given load spectrum, as defined by the Miner–Palmgren rule, the total damage a glider accumulates over time can be expressed as:
$$
D = t \cdot D_{\text{unit}},
$$

where:

$$D$$  is the total accumulated damage,

$$t$$  is the flight time,

$$D_{unit}$$  is the damage per hour under a specific load spectrum.



##### 3.3.2.2 Remaining real life and Miner-Palmgren ratio

Let:

$$D_\text{unit real}$$  = damage accumulated from actual flight load spectrum in 1 hour

$$D_\text{unit theoretical}$$ = damage predicted by the certified Kossira & Reinke load spectrum in 1 hour

$$t_{remaining\;theoretical}$$ = flight time remaining until the certified 12,000 hours are reached (under theoretical spectrum usage)

$$t_{remaining\;real}$$ = estimated remaining life under actual usage

$$D_{\text{remaining}}$$ = damage potential remaining until the certification limit $${D = \frac {1}{3}}$$ is reached

For a given remaining damage potential $$D_{\text{remaining}}$$, the time required to consume it, differs based on the spectrum used:

- Under the certified (theoretical) spectrum:
  $$
  t_{\text{remaining theoretical}} = \frac{D_{\text{remaining}}}{D_{\text{unit theoretical}}}
  $$

- Under the actual (real) measured flight data:
  $$
  t_{\text{remaining real}} = \frac{D_{\text{remaining}}}{D_{\text{unit real}}}
  $$

and define the Miner–Palmgren damage ratio \(R\) as:
$$
\boxed{R = \frac{D_{\text{unit theoretical}}}{D_{\text{unit real}}}}
$$

Substituting into the previous expression:
$$
t_{\text{remaining real}} = t_{\text{remaining theoretical}} \times R
$$

Thus, if real-world flights result in significantly lower damage per hour than the conservative certified assumption, the remaining life is proportionally extended.




##### 3.3.2.3 Additional life

The additional flying time enabled by lower real-world fatigue loads is:
$$
t_{extension} = t_{remaining\;real} - t_{remaining\;theoretical}\\
\\
\boxed {
t_{extension} = (R - 1) \times t_{remaining\;theoretical}
}
$$
To ensure the Miner–Palmgren ratio $$R$$  is valid, both damage values must be computed over the same duration (e.g., the same number of flight hours).

For our  specific problem, $$R$$ should be estimated using the data from real spectrum, which by definition has a duration of $$t_\text{real}$$ , and the data from the theoretical spectra, normalized to the same  $$t_{real}$$ hours:

- $$t_{real}$$ = duration of real flight data collected (in hours)
- $$D_{real}$$ = damage accumulated from actual flight load spectrum in  $$t_{real}$$ hours
- $$D_\text{theoretical}$$ = damage predicted by the certified Kossira & Reinke load spectrum in  $$t_{real}$$ hours

$$
D_\text{theoretical} = D_\text{unit theoretical}\times t_\text{real}
\\
D_\text{real} = D_\text{unit real} \times t_\text{real}
\\
R = \frac{D_\text{theoretical}}{D_\text{real}}
$$

If the theoretical spectrum has been calculated over the typical 6000 flight hours, for $$R$$ calculation, it should be normalized to the  time used for real spectrum observation  $$t_\text{real}$$ , using $$⌊ \frac{ni, theoretical \times t_{real}}{6000}⌋$$. The purpose of using the lower  integer part of a real number (denoted **⌊   ⌋**), is to provide additional conservatism when adjusting the $$n_i$$ of the theoretical spectrum to the same time exposure as the real flight data, as the later is much smaller.
Therefore it is possible to calculate $$R$$:
$$
R = \frac {\sum_i {⌊ \frac{ni, theoretical \times t_{real}}{6000}⌋} \; \times \; { {|LF_i - {LF_\text{average,theoretical}}|^{-1/b}}}}{\sum_i {n_i,real}  \;\times\;{|LF_i - {LF_\text{average,real}}|^{-1/b}}}
$$
Where:
- $$n_{i,theoretical}$$ and $$n_{i,real}$$ are the number of occurrences at each load factor level $$LF_i$$ in the theoretical and real spectra, respectively.

- $$LF_{average}$$ is the mean load factor for the respective spectrum.

- $$b$$  is the slope of the $$S/N$$ curve.

  

$$
R = \frac {\sum_i {⌊ \frac{ni, theoretical \times t_{real}}{6000}⌋} \; \times \; { {|LF_i - {LF_\text{average,theoretical}}|^{-1/b}}}}{\sum_i {n_i,real}  \;\times\;{|LF_i - {LF_\text{average,real}}|^{-1/b}}}
$$

$$
\boxed{t_\text{extension} = t_\text{remaining \;theoretical} \times ( \frac {\sum_i {⌊ \frac{ni, theoretical \times t_{real}}{6000}⌋} \; \times \; { {|LF_i - {LF_\text{average,theoretical}}|^{-1/b}}}}{\sum_i {n_i,real}  \;\times\;{|LF_i - {LF_\text{average,real}}|^{-1/b}}} - 1)
}
$$



To illustrate the time extension estimation, if real damage over 25 hours is 0.000035, and theoretical damage is 0.0007  (i.e., $R = 20$), and the glider has 500 hours left before 12,000 hours under theoretical use, the extension is $$t_{\text{extension}} = 500 \times (20 - 1) = 9500 \, \text{hours} $$.

As the following paragraphs will show, despite the variability from glider to glider, due to airframe response to turbulences, type of operations,  as well as pilot skills, the $$R$$  factor can reach a few hundred.
To ensure significant life extension is achieved, especially when glider operations result in lower  $$R$$ value, it is recommended to start instrumentation as soon as possible. As an example, it might be wise to instrument the glider when the last 1000-hours check is performed, before reaching the 12,000-hour limit.

However, it should be understood that $$R$$ ratio and time extension are highly dependent on the way the glider is being flown. Gliders being flown aggressively, performing spin entry/recovery or other maneuvers requiring a wide load factor range, will have much less favorable time extension than the gliders being flown cross-country with pilots flying softly.
In essence, regardless of the mission profile, gentler flying techniques will result in a greater potential life extension.



#### 3.3.3  Material parameter $$b$$

It is interesting to note that, when the theoretical and real spectra are given, only the parameter $$b$$ of Basquin equation ( $$S/N$$ curve slope) has an impact on the damage and ratio calculation.
Here is a list of typical $$b$$ values used in glider constructions:

Glass Fiber Reinforced Polymer (GFRP) :

- Range for $$b$$  : -0.07 to -0.1    [15]  [16] 
- GFRP fatigue is dominated by progressive fiber-matrix debonding, matrix cracking, and fiber breakage. The lower value is driven by  fiber-matrix composites (typically epoxy) and off axis performance.

Carbon Fiber Reinforced Polymer (CFRP) :

- Range for $$b$$  : -0.04 to -0.10  [17]  [18] 

- CFRP has a slightly better fatigue resistance due to superior carbon fiber. Like GFRP, lower value is driven by  fiber-matrix composites (typically epoxy) and off axis.



To avoid taking into account gliders' specific materials and construction, we can choose the most conservative b value for all composite material i.e.   $$b = -0.15$$,  therefore    $$-1/b = 6.6$$. This value overestimates damage for CFRP but ensures worst-case safety for GFRP which is more often used on older gliders.

The equation for damage accumulation for the $$real$$ spectrum becomes:

$$
D_{real}\;=\;\frac{1}{C'}\sum_i {n_{i,real}} \;{\bigl|\mathrm{LF}_{i,real}-{LF_{average,real}}\bigr|^{6.6}}
$$

$$
where \;\;C' \;=\;3\;\sum_i n_{i,theoretical}\,\bigl|\mathrm{LF}_{i,theoretical}-{LF_{average,theoretical}}\bigr|^{6.6}
$$

As long as $$D_{real}$$ stays below  $$\frac{1}{3}$$, the glider can continue operations.



The equation for the life extension becomes:
$$
\boxed{t_\text{extension} = t_\text{remaining theoretical} \times ( \frac {\sum_i {⌊ \frac{ni, theoretical \times t_{real}}{6000}⌋} \; \times \; { {|LF_i - {LF_\text{average,theoretical}}|^{6.6}}}}{\sum_i {n_i,real}  \;\times\;{|LF_i - {LF_\text{average,real}}|^{6.6}}} - 1)}
$$

From a fatigue standpoint, this is a very conservative and safe approach, which provides significant safety margin.

It should be noted that Miner-Palmgren rule and the $$S/N$$ curves are agnostic of the material being used.
We could also consider the metallic parts using a typical Basquin parameter for Aluminum  $$b= -0.2$$,    $$-1/b = 5$$ ,  and apply the same calculation method to metallic parts. 



## 4. Results and discussion

### 4.1 Comparative occurrences analysis

Preliminary calculations performed on a Janus B glider indicate that the real load spectrum produces significantly lower load factor occurrences than the theoretical model predicts. This reduction in load factor occurrences also translates into lower cumulative damage. The corresponding  damage ratio supports the potential for life extension.

The theoretical and real spectra plotted in Figure 9 highlight this opportunity for life extension. The theoretical load spectrum used as a reference is the flight only Kossira & Reinke spectrum which is their spectrum with least occurrences of least amplitude. This results in a more conservative life extension calculation which has the potential to be improved when the final reference spectrum is selected.



### 4.2 Miner-Palmgren, damage accumulation and  ratio evaluation

The simplified ratio:
$$
R = \frac {\sum_i {⌊ \frac{ni, theoretical \times t_{real}}{6000}⌋} \;\times\;{ {|LF_i - {LF_\text{average,theoretical}}|^{6.6}}}}{\sum_i {n_i,real}  \;\times\;{|LF_i - {LF_\text{average,real}}|^{6.6}}}
$$
provides a direct method to evaluate the difference in damage accumulation. Since real flight loads are less severe than those predicted by the Kossira & Reinke distribution, $R$ is expected to be significantly greater than one, thereby justifying an extension in the glider’s operational life.

The following is an example of  calculations performed with the conservative value of $$-1/b = 6.6$$, corresponding to worst-case GFRP structures.

A very preliminary analysis has been performed on several flights with different pilots on a Janus B.
The recording performed at 20 Hz sample rate, was processed using Kossira & Reinke counting method.

Using the Janus B data and the Kossira & Reinke reference spectrum, table 2 provides the different steps to compute the damage ratio. Because of the limited data, this table should be considered more like an illustration of the method.



![](C:\Users\JLD\Downloads\12000\life JANUS k=6.6 v3.jpg)

​								Table 2: Miner-Palmgren ratio and life extension calculation



In this table the parameter K = $$-1/b$$ , corresponds to the slope of the $$S/N$$ curve and the Basquin parameter.

The damage ratio is simply the ratio of the $$Kossira \; occ * |n - avg|^K$$  column and $$ JANUS \; occ * |n - avg|^K$$ column sum.

where 

$$Kossira \; occ * |n - avg|^K$$ corresponds to   $${\sum_i {⌊ \frac{ni, theoretical \times t_{real}}{6000}⌋} \;\times\;{ {|LF_i - {LF_\text{average,theoretical}}|^{6.6}}}}$$

$$ JANUS \; occ * |n - avg|^K$$   corresponds to   $$\sum_i {n_i,real}  \;\times\;{|LF_i - {LF_\text{average,real}}|^{6.6}}$$



As seen on Table 2 example, the ratio between the Kossira & Reinke and real flights damage accumulation is at 32.
Assuming the glider continues to operate with a similar load spectrum until it reaches 12,000 hours (i.e. in ~300 hours), the life extension would be around 9600 hours ( 32 x 300 ).

The table 2 example can also be used to help understand the sensitivity of the Miner ratio $$R$$ to the type of flight operations. If you imagine a pilot who would perform a constant 4g loop every two hours of flying, because the table 2 data is normalized to 6000 hours, this would add 3000 occurrences to classes 17 to 26 and, would reduce the $$R$$ ratio example from 32 down to 2.
This illustrates that the proposed method will justify life extension according to the use of the glider, and that a few high load maneuvers will have a significant effect on the $$R$$ ratio, as per Miner rule.  It should be noted that the  $$R$$ ratio of 2, due to the loops, is not accurate since the reference cycle, used for calculations, is a flight only, without aerobatic, spectrum. The purpose of the illustration is only to show that the $$R$$ ratio obtained when flying normally would be reduced by a factor of 16 due to aggressive maneuvers. 

This study focuses on composite gliders parts, hence the conservative GFRP $$6.6$$ Basquin parameter. It is however interesting to note that, if a more conservative Basquin parameter, typical to aluminum alloys : $$-\frac{1}{b} = 5$$  is used, we still obtain a very significant ratio of 12. This could be used to estimate the metallic parts life extension which would be around 3600-hours (12 x 300 ), based on the Janus data. This is significantly more than the repetitive 1000 hours inspections, currently required after 9000 hours. This legitimizes the continuation of these recurring inspections at 13,000 hours, 14,000 hours and beyond.
It should also be noted that, contrary to the composite structures, these metallic parts (wing shear pins and bushings, spar pins and bushings, tail fittings, etc.) can generally be inspected and eventually replaced during the repetitive inspections, reducing further risk of failure. 



### 4.3 Practical implications, safety and certification

Using this novel Structural Life Monitoring method, it is possible to tailor a given glider life, beyond the initially certified 12,000-hour limit, by function of its specific usage. This life limit extension is achieved while maintaining the level of damage accumulation accepted during certification.
EASA has already accepted several methods to comply with fatigue strength regulation requirements. This legitimizes SLM as an additional alternative solution, for aging gliders. 
EASA Certification Memorandum CM‑S‑006 endorses the use of Kossira & Reinke spectrum which have been designed to cover all types of usages, including some operations which are rarely flown by most gliders. While the proposed solution is consistent with these EASA reference load spectra and maintains significant calculation margins ( use of conservative Spectrum and Basquin $$b$$ parameter )  we still anticipate a large difference between the measured and the theoretical damage accumulations. This  has been confirmed during initial tests on several instrumented gliders. Still, the exact extension granted by the proposed SLM method will account for actual glider use, on a serial number basis.

As the life increase is proportional to the time the real spectrum is observed, it is advisable to instrument gliders as soon as possible and before they reach 12,000 hours, to be able to gain significant life extension.
Early life instrumentation might not be necessary when solely considering aging glider life extension, but would provide valuable data and statistics, in the understanding of glider usage. 

#### 4.3.3  Concept of Operation proposals

##### 4.3.3.1 Project proposal

The gliders should enter the project with a valid CoA before having reached 12,000 hours.
Each glider should have a person designated to supervise the operation of this glider.
The acceleration recording equipment will be installed using CS-CSTAN 104b, which should appear on the logbook to ensure the glider time is known when the recorder has been installed.
On a regular basis, e.g. every week when there is activity, the recorder files and the logbook of the glider will be transmitted to the project leader who will process them. 
If some of the gliders are at risk of reaching the 12,000-hour limit during the experimentation, a third party (e.g. FFVP/APDOA) will apply for a Permit to Fly (PtF) or limited Supplemental Type Certificate (STC) specific to the serial number (s/n), to allow continuation of operation. This is with the assumption that the damage accumulation is providing sufficient margin. In the case of PtF, it should allow all required types of operations to continue experimentation.
The analysis tools and algorithms will be matured and distributed openly.
Reports, including flights evaluations as well as technical points required to deploy the solution, will be sent to the project participants at least on a quarterly basis.

The main deliverables of the project should be:

- validation of the SLM damage calculation estimations
- selection of the reference spectrum
- selection of the Basquin composite material properties
- modeling of the special flight phases, when non-aerodynamic forces are applied to the glider
- recording equipment minimum performance requirements, including maintenance/performance validation during operation
- algorithms, tools and logistic, capable of processing recorders file to provide the data necessary to decide if glider's damage accumulation is within acceptable limit, and life limit extension estimation compatible with next scheduled visit.
- definition of the fatigue recurring inspections (content/timing) required to continue operations. This could be based on the existing recurring inspections, which scope could be extended based on manufacturer's experience.
- Alternative Means of Compliance (AltMOC) and associated concept of operations (CONOPS) approved by EASA

##### 4.3.3.2 Deployment proposal

Once EASA has formalized a path to use SLM as a valid Means of Compliance, thanks to the project deliverables, the TC owners or third parties will be able to  propose solutions with minimal effort.
For TC owners, they will be able to develop modifications and Service Bulletins (SB) to install the required equipment.
For third parties, they will be able to develop STC, similar to the STC developed within the project.
In both cases, they or a third party, will have to provide the framework required to allow the glider owners to report their activity and, in return, get the authorization to perform the recurring inspections and continue operation.
TC or STC owners will have open access to the project deliverables, algorithms and software solutions if they elect to develop their own framework or use the services of a third party.
Typical CONOPS for deployment could be:

- Application of SB or STC, while glider has not reached the initial 12,000-hour limit. These SB or STC would describe in detail the process required to maintain airworthiness. The following list is an example of what the method could be.
- Transmission on a regular basis, of glider logbook and recorder files to the party in charge of validating SLM data.
- At every maintenance activity, include the SLM reports provided by the party in charge, to the glider maintenance records (e.g. Airworthiness Review Certificate (ARC), recurring 1000-hour inspection, etc.). These reports would include the calculation of the remaining damage potential as well as an estimation of the life potential based on current usage.
- The sensor performance is verified at a regular interval, during one of the scheduled inspections (e.g. recurring fatigue inspection, annual inspection, etc.).
- When the glider reaches the initial 12,000-hour limit,  all previous activities required to maintain CoA continue.
- A new life inspection visit is added to the maintenance schedule, with a first occurrence at 12000 hours. Its schedule is based on the SLM report and could not exceed the calendar limit of the ARC. The goal of this visit is to ensure the remaining damage potential is not exhausted before next scheduled visit.
- The updated recurring fatigue inspection program is also included in the glider maintenance schedule.
- This process continues until the glider has exhausted its remaining damage potential, and is retired from service.



## 5. Conclusion

This study outlines a methodology for extending the operational life of gliders using Structural Life Monitoring.
Measurement of flight accelerations, processed with the Miner-Palmgren rule, allows computation of damage accumulation. As long as the real damage accumulation does not exceed the end of life theoretical damage accumulation defined during certification, operation could continue. Additionally, the ratio  between the reference and real damage could be used to predict life extension, beyond 12,000 hours.
The initial results show that, even when selecting conservative calculation methods and material fatigue parameters, damage accumulation from actual flights is orders of magnitudes lower than damage accumulation predicted by the theoretical models.
The corresponding  significant life increase is in line with life limits experienced on similar composite structures  from other industries, like wind turbines. It is also in line with the assessment performed by TRAFI (Finland) in 2015, setting the PIK20D glider life to 65,000-hour. 
However, it should be clear that gentler flying results in greater life extension.

This approach maintains **Safety level** (method is conservative, maintains certified limits), offers **Economic benefits** (extends asset life) and **Environmental benefits**  (reduces waste), and is compatible with EASA fatigue strength regulation requirement and means of compliance. It is however advisable to first experiment this approach on a selected fleet of instrumented gliders, which could be monitored closely to confirm the initial results. The solution could then be finalized and, after approval by EASA as an acceptable alternative means of compliance, deployed on any aging glider, using Supplemental Type Certificates or Service Bulletins.

.

## References

1. Kossira, H. and Reinke, W. (OSTIV Publication XVI). “Determination of load spectra for the design of sailplanes.”

2. Kossira, H. (1982). “Determination of load spectra and their application for keeping the operational life proof of sporting airplanes.” *ICAS-Proc. 8/1982; ICAS-82-2.8.2*, pp. 1330-1338.

3. EASA Certification Memorandum CM‑S‑006, *Certification, Type Design Definition, Material and Process Qualification for Composite Light Aircraft*. [Available at: [EASA Document Library](https://www.easa.europa.eu/en/document-library/product-certification-consultations/easa-cm-s-006)]

4. Pommera, G. (2000). *Minutes of LBA/DGAC meeting dedicated to 12,000 hours gliders fatigue life – November 14, 2000*.

5. LBA Document, *German LBA Standards for Structural Substantiation – Master*.

6. Easy Access Rules for Very Light Aeroplanes (CS-VLA)  /  EASA AMC VLA 572

7.  Kensche, C (2019). Numerical Comparison of Glider Load Spectra Christoph TECHNICAL SOARING

8.  Soinne , Erkki (2015), PIK-20D Fatigue evaluation, Trafi Research Reports Trafin tutkimuksia Trafis undersökningsrapporter 7/2015

9.  C.A. Patching & L.A Wood (1991). Fatigue testing of a GFRP glider, OSTIV Congress, Uvalde, Texas, U.S.A.

10. Standard practices for cycle counting in fatigue analysis. ASTM E 1049-85.

11. Kossira H., Reinke W., Festigkeit von modernen GFK-Konstruktionen für Segelflugzeuge - Bestimmung eines Belastungskollektives, IFL-IB 84-01 Technische Universität Braunschweig

12. Miner, M. A. (1945). *Cumulative Damage in Fatigue.* Journal of the Engineering Mechanics Division.

13. Palmgren, A. (1947). *A Probabilistic Theory of Cumulative Damage.* [Journal/Conference details].

14. Basquin, O.H. (1910).  "The exponential law of endurance tests." Proceedings of the ASTM, Vol. 10, pp. 625–630.

15. Mandell, J. F. (1982). *Fatigue Behavior of Fiber Resin Composites*. Elsevier.

16. Harris, B. (2003). *Fatigue in Composites: Science and Technology of the Fatigue Response of Fibre-Reinforced Plastics*. Woodhead Publishing.

17. Talreja, R. (1985). *Fatigue of Composite Materials*. Technomic Publishing.

18. Bathias, C. (1999). *Fatigue of Materials and Structures: Application to Design and Damage*. Wiley.

    