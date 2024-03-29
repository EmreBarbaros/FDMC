
# FDMC
\
**Spectral disentangling using [MCMC](https://aip.scitation.org/doi/pdf/10.1063/1.1699114) optimization with [FDBinary](http://sail.zpf.fer.hr/fdbinary/)**.
\
\
Spectral disentangling is a mathematical method for obtaining the spectra of the component stars that make up spectral binary star systems. The radial velocities of the components in each observation are calculated and then a radial velocity correction is performed.
\
\
<img src="https://user-images.githubusercontent.com/100410767/210554256-66f9dab0-1066-47c7-8cb1-da97ae0c4e50.jpg" width=100% height=30%>
\
\
The method uses orbital parameters of the binary system. This parameters are; orbital period of binary system **P**, periastron passage **T0**, eccentricity of orbit **e**, longitude of periastron **ω** and radial velocities of components **K1**,**K2**. [FDBinary](http://sail.zpf.fer.hr/fdbinary/), performs a orbit simulation using these parameters and calculates the velocities of the components for each observation. An optimization routine is needed to determine the parameters most accurately. [FDBinary](http://sail.zpf.fer.hr/fdbinary/) is using [Downhill - Simplex Method](https://people.duke.edu/~hpgavin/cee201/Nelder+Mead-ComputerJournal-1965.pdf) for optimization. This routine is have some problems and cannot perform error analysis.

FDMC is a code written to solve this problem. Uses [FDBinary](http://sail.zpf.fer.hr/fdbinary/) for spectral disentangling and uses [MCMC](https://aip.scitation.org/doi/pdf/10.1063/1.1699114) algorithm for parameter optimization. [MCMC](https://aip.scitation.org/doi/pdf/10.1063/1.1699114) is to strong optimization routine and can perform error analysis with Bayesian statictic. FDMC is work on [Linux](https://www.linux.org/) systems and can work multiprocess. It stores the result of each iteration in it and this makes analysis easier.

<p align="center">
    <img src="https://user-images.githubusercontent.com/100410767/210587255-b7721411-e4f2-4877-956d-32870c5c3c53.gif" width=60% height=60%>
</p>

FDMC using [corner plot](https://www.researchgate.net/publication/303872046_cornerpy_Scatterplot_matrices_in_Python/fulltext/5a2cd23ba6fdccfbbf8746e5/cornerpy-Scatterplot-matrices-in-Python.pdf) for error analysis. In this way, the distribution of parameters in optimization space can also be seen. Additionally FDMC includes other different analyses within.

<p align="center">
    <img src="https://user-images.githubusercontent.com/100410767/211144344-7a6da86a-bb46-4785-a280-7e99ff8910d2.jpg" width=50% height=30%>
</p>

For more details about *"spectral disentangling"* and *"FDMC"* , you can visit  [**This Page**](https://tez.yok.gov.tr/UlusalTezMerkezi/TezGoster?key=RsTBl6RWK25OBMIKtIgYYfD8JcyyaT6TuRGpUGHqr4h-s1UXQCjI-5aUytqxUzIi).
