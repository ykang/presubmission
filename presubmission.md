--- 
title       : Events in turbulence time series
subtitle    : Presubmission review seminar 
author      : Yanfei Kang 
job         : Supervised by Prof. Kate Smith-Miles and Dr. Danijel Belusic
framework   : io2012   # {io2012, html5slides, shower, dzslides, ...}
highlighter : highlight.js  # {highlight.js, prettify, highlight}
hitheme     : tomorrow      # 
widgets     : mathjax
mode        : selfcontained # {standalone, draft, selfcontained}
transition  : fade

--- bg:#f5f5ae




## Introduction

### - Motivation

### - Difficulties

### - Objectives 

---
## Motivation

<img src="assets/fig/chunk0.pdf" title="plot of chunk chunk0" alt="plot of chunk chunk0" style="display: block; margin: auto;" />


- Event <u>detection</u>, <u>classification</u> and <u>interpretation</u> in  turbulence time series.

  - Location?
  - Similar?
  - Physical mechanisms?

--- 

## Difficulties

- Red noise
- Varibility of spatial and temporal scales.
- Previously unknown.
- Small amount of literature.


--- 

## Objectives 

>1. Develop a method to detect and classify events:
  - does not require any pre-assumptions of events.
  - deal with high noise.
  - not limited by  stability or scales. 
>2. Application of the method on a well-known dataset
  - also a validation of the method.
>3. Use the method to
  - detect events in the unknown stable atmospheric boundary layer (ABL).
  - find  physical  dynamics of different types of events.
  - study the effects of the event to the turbulence flows.  
>4. Develop a statistical tool and make it easy to use for others.

---

## The journey 

<div align="center">
<img src="timeline.pdf" height="500" width="1000">
</div>

--- bg:#f5f5ae 

## Chapter 2

<p>Kang Y (2012).
&ldquo;Real-time change detection in time series based on growing feature quantization.&rdquo;
In <EM>Proceedings of the 2012 International Joint Conference on Neural Networks (IJCNN)</EM>, pp. 1&ndash;6.
IEEE.




--- &twocol
## An example

*** =left
<div>
<img src='nile.png' width=460,height=450>
</div>

*** =right
<div>
<img src='nileD.png' width=460,height=450>
</div>

--- bg:#f5f5ae
## Chapter 3

<p>Kang Y, Belusic D and Smith-Miles K (2014).
&ldquo;A note on the relationship between turbulent coherent structures and phase correlation (Resubmitted after revision).&rdquo;
<EM>Chaos: An Interdisciplinary Journal of Nonlinear Science</EM>.


--- bg:#f5f5ae
## Chapter 3

<p>Kang Y, Belusic D and Smith-Miles K (2014).
&ldquo;A note on the relationship between turbulent coherent structures and phase correlation (Resubmitted after revision).&rdquo;
<EM>Chaos: An Interdisciplinary Journal of Nonlinear Science</EM>.


## What are events? Characteristics?

### Coherent structures

- A typical type of events

- Generally used assumption: phase correlation

- Really? Can we use that to detect events?

---
## Not really! Why?

- Coherent structures detected using wavelets method
- Measure their phase correlation.
- How? Using surrogates.

---
## Surrogates of $x_O(t)$


>1. phase randomized surrogate $x_R(t)$
  - take the Fourier Transform of $x_O(t)$.
  - randomize phase information while keeping the magnitude.
  - do inverse Fourier Transform to get back to time domain to get $x_R(t)$.
  - none phase correlation.

>2. completely coherent surrogate $x_C(t)$
  - obtained by making the phases constant.
  - largest phase correlation

---
## Measure of phase correlation I
### Coherece index ($CI$)

Given $x_O(t)$, $x_R(t)$ and $x_C(t)$,

$$CI(q,\tau)=\left(\frac{|S_O(q,\tau)-S_R(q,\tau)|}{|S_O(q,\tau-S_R(q,\tau))|+|S_O(q,\tau)-S_C(q,\tau)|}\right)^{1/q},$$
where $S_i(q,\tau)$ is the $q$th order structure function: $S_i(q,\tau)=\left<|x_i(t+\tau)-x_i(t)|^q\right>$, $i \in \{O, R, C\}$ and $\tau$ is the time lag.


---
## Measure of phase correlation II

### Nonlinearity Measure Based on Nonlinear Prediction Error ($nm_{npe}$)
\[
X=
  \begin{bmatrix}
    x(1) & x(2) & \cdots & x(m) \\
    x(2) & x(3) & \cdots & x(m+1) \\
    \cdots & \cdots & \cdots & \cdots \\
    x(n-m+1) & x(n-m+2) & \cdots & x(n) \\
  \end{bmatrix}
\] 

For each row (delay vector) of $X$, its $k$ nearest $m$-dimensional delay vectors are found using Euclidean distances. If the $k$ nearest delay vectors for  $\vec{x}_i$ are $\vec{x}_{j_p}$, $p=1, 2, \cdots, k$, the nonlinear prediction error for the time series $x(t)$ is defined as 
$$
\tau_X(m, k)= \sum\limits_{i=1}^{n-m}\left(x(i+m) - \frac{1}{k}\sum\limits_{p=1}^k x(j_p+m)\right)^2.
$$

---
## Measure of phase correlation II

### Nonlinearity Measure Based on Nonlinear Prediction Error ($nm_{npe}$)

$$
nm_{npe}=\frac{\bar{\tau}_R-\tau_X}{3\sigma_{R}},
$$
where $\tau_X$ is the nonlinear prediction error of the original data, while $\bar{\tau}_R$ and $\sigma_R$ are the mean and standard deviation of the nonlinear prediction errors of the surrogates. 

$$
\begin{aligned}
& \\
&x(t) \text{ is } \begin{cases}
  \text{phase-correlated,} & \text{if } nm_{npe} \geq 1, \\
  \text{phase-uncorrelated,} & \text{otherwise}.
\end{cases}
\end{aligned}
$$


---
## Results
<div align="center">
<img src="hist.pdf" width=800, height=400>
</div>

---
## Conclusion



>- the space and time organized structures in turbulent flow do not necessarily have correlated phases.

>- quantitative way of event description difficult.

>- then?





--- bg:#f5f5ae

## Chapter 4

<p>Kang Y, Smith-Miles K and Belusic D (2013).
&ldquo;How to extract meaningful shapes from noisy time-series subsequences?&rdquo;
In <EM>Proceedings of the 2013 IEEE Symposium on Computational Intelligence and Data Mining (CIDM)</EM>, pp. 65-72.
IEEE.


--- bg:#f5f5ae

## Chapter 4

<p>Kang Y, Smith-Miles K and Belusic D (2013).
&ldquo;How to extract meaningful shapes from noisy time-series subsequences?&rdquo;
In <EM>Proceedings of the 2013 IEEE Symposium on Computational Intelligence and Data Mining (CIDM)</EM>, pp. 65-72.
IEEE.


## Focus shifted

<div align='center'>
<img src='shift.pdf',width=1000,height=500>
<div>

---
## Artificial time series


  
<img src="assets/fig/chunk1.pdf" title="plot of chunk chunk1" alt="plot of chunk chunk1" style="display: block; margin: auto;" />




<img src="assets/fig/chunk2.pdf" title="plot of chunk chunk2" alt="plot of chunk chunk2" style="display: block; margin: auto;" />




---

## Methodology: two steps


1. Detect events.

2. Cluster the detected events.



---

## $1$st step: event detection 

- Perform  noise test on each subsequence.


  >- Why? Only care the non-noise subsequences.

  >- Then given a window length,  for the $q$th subsequence, get $p$-value $p_q$. For $x(t)$,  a $p$-value series:  $p_1,p_2,\cdots,p_{m-w+1}$.

--- 

## $p$-value series for the artificial data
<center>
#### Sliding window length: $w=128$
</center>
<img src="assets/fig/chunk4.pdf" title="plot of chunk chunk4" alt="plot of chunk chunk4" style="display: block; margin: auto;" />


---
## How to define events?

<img src="assets/fig/chunk4_1.pdf" title="plot of chunk chunk4_1" alt="plot of chunk chunk4_1" style="display: block; margin: auto;" />


- <span style=" border: 1px solid red;">*A potential event*</span> is a subsequence whose noise test $p$ value is smaller than a predefined significant level $\alpha$ ($\alpha=0.05$).

- Assume there exists a consecutive sequence of $p$ values $p_s,p_{s+1},\cdots,p_t$ which satisfies: 

  - $p_i\leq \alpha, i=s, s+1, \cdots, t$
  - $t-s\geq w/2$ 

    then we define the subsequence $x_{\left\lfloor\frac{t+s}{2}\right\rfloor}(t)$ as <span style=" border: 1px solid red;">*the event*</span> we are interested in.

--- 

## Showing how it works

<div align="center">
<img src="tsShapes.gif">
</div>

---

## Events extracted


<img src="assets/fig/chunk8.pdf" title="plot of chunk chunk8" alt="plot of chunk chunk8" style="display: block; margin: auto;" />


---

## Robust to noise?


<img src="assets/fig/chunk9.pdf" title="plot of chunk chunk9" alt="plot of chunk chunk9" style="display: block; margin: auto;" />





--- 

## 2nd step: event classification

#### Goal: cluster the extracted events into patterns. 


<div align="center">
<img src="shapeclustering.pdf" width=380, height=500>
</div>

--- &twocol w1:50% w2:50%

## Comparison with literature 

*** =left

<div align='center'>
<img src="motif13.pdf" width=400, height=600>
</div>

*** =right 

<div align='center'>
<img src="shapeclustering.pdf" width=360, height=500>
</div>




--- bg:#f5f5ae

## Chapter 5

<p>Kang Y, Belusic D and Smith-Miles K (2014).
&ldquo;Detecting and Classifying Events in Noisy Time Series.&rdquo;
<EM>Journal of the Atmospheric Sciences</EM>, <B>71</B>(3), pp. 1090&ndash;1104.


--- bg:#f5f5ae

## Chapter 5

<p>Kang Y, Belusic D and Smith-Miles K (2014).
&ldquo;Detecting and Classifying Events in Noisy Time Series.&rdquo;
<EM>Journal of the Atmospheric Sciences</EM>, <B>71</B>(3), pp. 1090&ndash;1104.


## What's done?

- Method improvement
- Application to a well known dataset
- Validation of the method

---
## Motivation

- Pratical problems: 
  - non-stationarity
  - turbulence intermittency
- AR(1) modelling --- stationarity
- Phillips-Perron (PP) Unit Root Test (<a href="">Perron (1988)</a>)

---
## Three cases of the unit root test 

- No trend, no drift:

$$X_t=\phi*X_{t-1}+u_t \: (H_0: \phi=1)$$

- No trend, drift 

$$X_t=\delta+\phi*X_{t-1}+u_t \: (H_0: \phi=1)$$

- Trend, drift 

$$X_t=\delta+a+b*t+\phi*X_{t-1}+u_t \: (H_0: \phi=1)$$

---

## PP Unit Root Test 



$$\triangle X_t=\beta' D_t+\pi*X_{t-1}+u_t,$$


$$ H_0: \pi = 0 \text{ (unit root)}$$ 
$$ H_1: \pi < 0 \text{ (stationary)}$$



- Drift and deterministic trend are considered in $D_t$.
- $X_t = \phi*X_{t-1}+u_t$.
- $\pi=0$ means  $\phi=1$ (unit root).


---

## Why PP?

- `adf.test` (test for unit root) 
- `kpss.test` (test for stationarity)
<img src="assets/fig/whypp.pdf" title="plot of chunk whypp" alt="plot of chunk whypp" style="display: block; margin: auto;" />


---


## Example: random walks

<img src="assets/fig/rw.pdf" title="plot of chunk rw" alt="plot of chunk rw" style="display: block; margin: auto;" />


---
## Example: stationary

<img src="assets/fig/st.pdf" title="plot of chunk st" alt="plot of chunk st" style="display: block; margin: auto;" />


---
## Problem

 Difficult to statistically distinguish between an I(1)–series (e.g.  $X_t = X_{t-1} + u_t$) from a stable I(0) that is contaminated by a structrual shift, for example:

 $$
\begin{aligned}
& X_t = 0.5*X_{t-1} + 20*DU_t + u_t, \\
&DU_t = \begin{cases}
  1, & \text{if } t > 500, \\
  0, & \text{otherwise}.
\end{cases}
\end{aligned}
$$


<img src="assets/fig/pp_problem.pdf" title="plot of chunk pp_problem" alt="plot of chunk pp_problem" style="display: block; margin: auto;" />


---

## Structure breaks

In the presence of a structural break, the tests are biased towards the non-rejection of the null hypothesis.

<img src="assets/fig/break.pdf" title="plot of chunk break" alt="plot of chunk break" style="display: block; margin: auto;" />


---

## ZA test

A unit root test which considers structure break: Zivot \& Andrews (ZA) unit root test (<a href="">Zivot & Andrews (1992)</a>)

Allow a break in the null and alternative:

$$
\begin{aligned}
&\triangle X_t=\pi*X_{t-1}+\theta*DU_t+\sum\limits_{j=1}^p \triangle X_{t-j}+u_t, \\
&DU_t = \begin{cases}
  1, & \text{if } t > TB, \\
  0, & \text{otherwise}.
\end{cases}
\end{aligned}
$$

---  &twocol w1:50% w2:50%

## ZA test example

*** =left

<img src="assets/fig/pp.pdf" title="plot of chunk pp" alt="plot of chunk pp" style="display: block; margin: auto;" />


*** =right

</br>
</br>


Percentage of unit-root steps using PP: 100%

Percentage of unit-root steps using ZA: 0%

</br>
</br>
</br>
</br>
</br>
Percentage of unit-root ramps using PP: 97.8%

Percentage of unit-root ramps using ZA: 1%



---

## The improved method

<div align="center">
<img src="flowchart.pdf" width=1000,height=600>
</div>


---

## Comparison with literature
### This is a comparison with wavelets method (<a href="">Thomas & Foken (2005)</a>).

<div align="center">
<img src="red.pdf" width=900,height=400>
</div>

---

## Using the method
### Testing the performance



- 1999 Cooperative Atmosphere–Surface Exchange Study (CASES-99) (<a href="">Poulos et al. (2002)</a>).

- 1-s averages of data from 1100 LST 5 October to 1100 LST 6 October ($l=86400$).

- validation by comparing the results with the previous studies.

 

--- 

## Event detection and clustering 

### 102 events detected and clustered using:

  - `Smoothness`: $\frac{\text{sd}(\text{diff}(x))}{\text{mean(diff}(x)}$
  - `diff kurtosis`:  kurtosis of diff($x$)
  - `diff Max`: $\text{max}(\text{diff}(x,\text{lag}=5))$
  - `diff Min`: $\text{min}(\text{diff}(x,\text{lag}=5))$
  - `sd`: measured in the same way as in the artificial time series
  - `Kurtosis`: measured in the same way as before
  - `Skewness`: measured in the same way as before
  - `Peroid`:  measured in the same way as before

--- &twocol w1:50% w2:50%

## Physical behaviors

*** =left
</br>


<div>
<img src="Transition.pdf" height="250" width="500">
</div>
</br>
<p>- Evolution of clusters  in line with that of stability.</p>

<p>- Distinction between deep and shallow events. </p> 
*** =right
<div>
<img src="Depths.pdf" height="550" width="450">
</div>



 




--- bg:#f5f5ae
## Chapter 6

<p>Kang Y, Belusic D and Smith-Miles K (2014).
&ldquo;Classes of Structures in the Stable Atmospheric Boundary Layer (Submitting soon).&rdquo;
<EM>Quarterly Journal of the Royal Meteorological Society</EM>.


---
## Application

- Motivation dataset --- FLOSS (<a href="">Mahrt (2011)</a>)

  - 130 nights
  - 9h per night
  - 6s averaged
  - $l=702000$

- Very stable unknown ABL. 

- No published results.

- Few studies on detailed physical analysis.

---
## FLOSS events and clustering
### 926 events detected and grouped into 3 clusters.

<div align="center">
<img src="pca_plot.pdf">
</div>

--- &twocol w1:50% w2:50%
## FLOSS event cluster prototypes
*** =left
<div>
<img src="prototypes.pdf" height="600" width="400">
</div>
*** =right
<div>
<img src="centroid.pdf" height="550" width="450">
</div>

---
## FLOSS events: physical characteristics

</br>

<center>

 Ri bins | Percentage of events
:------------------|:------------:
 Ri <= 0.25 | 19.1%
 0.25 < Ri < 1 | 42.0%
 Ri >= 1 | 23.5%

</center>

---
## FLOSS events: physical characteristics

<div align="center">
<img src="boxplots.pdf" height="550" width="400">
</div>

--- &twocol w1:50% w2:50%
## FLOSS events: physical characteristics
*** =left
<div>
<img src="boxplots_profiles_1.pdf" height="580" width="400">
</div>
*** =right
</br>
<div>
<img src="boxplots_profiles_2.pdf" height="460" width="400">
</div>

--- &twocol w1:60% w2:40%
## FLOSS events: deep and shallow events

*** =left
</br>
<div>
<img src="deepshallowtab.pdf" height="400" width="580">
</div>
*** =right
</br>
<div>
<img src="deep_and_shallow_shear.pdf" height="400" width="400">
</div>

--- &twocol w1:50% w2:50%
## FLOSS events: eg1 and eg2

*** =left

<div>
<img src="Cl1eg.pdf" height="580" width="400">
</div>
*** =right

<div>
<img src="Cl2eg.pdf" height="580" width="400">
</div>

--- &twocol w1:50% w2:50%
## FLOSS events: eg3 and hodograph

*** =left

<div>
<img src="Cl3eg.pdf" height="580" width="400">
</div>
*** =right

<div>
<img src="hodograph.pdf" height="250" width="500">
</div>


--- bg:#f5f5ae
## Chapter 7


<p>Kang Y, Belusic D and Smith-Miles K (2014).
&ldquo;Detecting Events from Very Noisy Time Series with the R package <span class="pkg">TED</span>  (In preparation).&rdquo;
<EM>Journal of Statistical Software</EM>.


- R package to share our work with the community

- https://github.com/ykang/TED

--- bg:#f5f5ae
## Conclusion
### Event detection, classification and interpretation in turbulence.

--- bg:#f5f5ae
## Conclusion
### Event <u>detection</u>, <u>classification</u> and <u>interpretation</u> in turbulence.
<div align='center'>
<img src='conclusion.pdf',width=1000,height=600>
</div>

---
## References
<p>Kang Y (2012).
&ldquo;Real-time change detection in time series based on growing feature quantization.&rdquo;
In <EM>Proceedings of the 2012 International Joint Conference on Neural Networks (IJCNN)</EM>, pp. 1&ndash;6.
IEEE.

<p>Kang Y, Smith-Miles K and Belusic D (2013).
&ldquo;How to extract meaningful shapes from noisy time-series subsequences?&rdquo;
In <EM>Proceedings of the 2013 IEEE Symposium on Computational Intelligence and Data Mining (CIDM)</EM>, pp. 65-72.
IEEE.

<p>Kang Y, Belusic D and Smith-Miles K (2014).
&ldquo;A note on the relationship between turbulent coherent structures and phase correlation (Resubmitted after revision).&rdquo;
<EM>Chaos: An Interdisciplinary Journal of Nonlinear Science</EM>.

<p>Kang Y, Belusic D and Smith-Miles K (2014).
&ldquo;Detecting and Classifying Events in Noisy Time Series.&rdquo;
<EM>Journal of the Atmospheric Sciences</EM>, <B>71</B>(3), pp. 1090&ndash;1104.

<p>Kang Y, Belusic D and Smith-Miles K (2014).
&ldquo;Classes of Structures in the Stable Atmospheric Boundary Layer (Submitting soon).&rdquo;
<EM>Quarterly Journal of the Royal Meteorological Society</EM>.


---
## References

<p>Kang Y, Belusic D and Smith-Miles K (2014).
&ldquo;Detecting Events from Very Noisy Time Series with the R package <span class="pkg">TED</span>  (In preparation).&rdquo;
<EM>Journal of Statistical Software</EM>.

<p>Mahrt L (2011).
&ldquo;Surface Wind Direction Variability.&rdquo;
<EM>Journal of Applied Meteorology and Climatology</EM>, <B>50</B>(1), pp. 144&ndash;152.

<p>Poulos GS, Blumen W, Fritts DC, Lundquist JK, Sun J, Burns SP, Nappo C, Banta R, Newsom R, Cuxart J, Terradellas E, Balsley B and Jensen M (2002).
&ldquo;CASES-99: A Comprehensive Investigation of the Stable Nocturnal Boundary Layer.&rdquo;
<EM>Bulletin of the American Meteorological Society</EM>, <B>83</B>(4), pp. 555&ndash;581.

<p>Perron P (1988).
&ldquo;Trends and random walks in macroeconomic time series: Further evidence from a new approach.&rdquo;
<EM>Journal of economic dynamics and control</EM>, <B>12</B>(2), pp. 297&ndash;332.

<p>Zivot E and Andrews DWK (1992).
&ldquo;Further evidence on the great crash, the oil-price shock, and the unit-root hypothesis.&rdquo;
<EM>Journal of Business \&amp; Economic Statistics</EM>, <B>20</B>(1), pp. 25&ndash;44.

<p>Thomas C and Foken T (2005).
&ldquo;Detection of Long-term Coherent Exchange over Spruce Forest Using Wavelet Analysis.&rdquo;
<EM>Theoretical and Applied Climatology</EM>, <B>80</B>, pp. 91-104.


---
<center>
## Questions?
</br>
<div align='center'>
<img src="http://i.imgur.com/wjyiL.jpg" width="700" height="500">
</div>
