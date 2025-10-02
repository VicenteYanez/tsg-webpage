---
layout: work
---
# Solutions

We are developing a SaaS web platform that delivers flexible and reliable **3‑D magnetotelluric (MT)** models by combining **deep‑learning** frameworks with **Bayesian inference**. Our solution reduces computing time and costs while providing geologically plausible results.

## Development status

Our technology is currently at **TRL 5** (validated in a relevant environment), meaning that the components work together in a prototype that reflects real‑world operating conditions.

Our current tests with the dataset of Díaz et al. (2015) demonstrate that our approach can be applied to a high‑dimensional inversion of **> 1 million parameters**, covering 30 stations and 18 periods for the XY and YX components. The **inversion converges in just 20 hours** of computation on an AMD Ryzen 9 9950X (16 cores), 64 GB RAM, and an NVIDIA GeForce RTX 4090.

The recovered model (shown below as two orthogonal profiles, EW and NS) exhibits reasonable agreement between predictions and observations, indicating that the development is progressing correctly. The main geophysical features are consistent with the published model:

![Modelo MT]({{ site.baseurl }}/assets/img/content/modelo_data.png)

- Resistivity values span a comparable range of roughly 1 – 1000 Ω·m and increase toward the east.
- High‑conductivity bodies extend to depths of up to 4 km and are predominantly oriented N‑NE.

### Main limitation

The current algorithm does not explore the solution space exhaustively; generated models tend to collapse into a single electrical‑resistivity configuration. This acts as an implicit regularization that captures only first‑order subsurface structures, leaving local heterogeneities unrecovered. Consequently, the final output is an **averaged model** that reflects the overall trend rather than fine‑scale geological detail.

---

*Future work will focus on improving the sampling strategy to better capture multi‑modal posterior distributions and recover finer heterogeneities.* 
