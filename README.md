# matrix-population-models
A loose collection of theoretical and applied work on **matrix population models** (MPMs). This repository stems from a personal interest in MPMs, which help me in my professional activities at the [Research Institute for Nature and Forest](https://www.vlaanderen.be/inbo/en-gb/homepage/) (Belgium). MPMs play an important role in the support my Institute provides to local, national and European stakeholders regarding the management of **invasive species** and **game species**. Given the public interest of such work, please feel welcome to suggest comments or corrections, or use code, within this repo.

## The basics

> Caswell, H. (2001). Matrix population models: construction, analysis, and interpretation. 2nd edition. Sinauer Associates, USA. 722 pp.

> Stott, I., _et al._ (2012). popdemo: an R package for population demography using projection matrix analysis. Methods in Ecology & Evolution, 3: 797-802.

> Jones, O., _et al._ (2022). Rcompadre and rage: two R packages to facilitate the use of the COMPADRE and COMADRE databases and calculation of life‐history traits from matrix population models. Methods in Ecology and Evolution, 13: 770-781.

Undeniably the 'bible' on the subject, Caswell (2001) provides a definitive overview of the mathematical foundations of MPMs, and all their possible applications. Fortunately, all standard MPM operations have become accessible through the excellent [popdemo](https://github.com/iainmstott/popdemo) R package (Stott _et al._ 2012). Also, numerous population matrices can now be easily accessed via the [rcom(p)adre](https://github.com/jonesor/Rcompadre) package (Jones _et al._ 2022). In effect, this repository is anticipated to contain several applications of these package, or snippets of code beyond them.

## Hastings _et al._ (2006) Theor. Pop. Biol

> Hastings, A., Hall, R. J., & Taylor, C. M. (2006). A simple approach to optimal control of invasive species. Theoretical population biology, 70(4), 431-435.

Hastings _et al._ (2006) have extended MPM's base formula to grasp the situation where a population's trajectory is affected by recurrently _removing_ individuals, rather than by affecting _vital rates_ directly. The equation is then used for the optimization of population control, through linear programming techniques. Such removal-based management is the standard approach to invasive species control, but in practice, calculations are almost never made...

$$N_{T} = L^TN_{0}-\sum_{i=1}^{T}L^{T+1-i}H_{i}$$

Under ```file```, I develop and illustrate the use of this equation.
