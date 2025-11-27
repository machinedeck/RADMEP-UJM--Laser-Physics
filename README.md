# Laser Physics
<p align = "center"><img src = "images/ujm-radmep-logo.png"></p>

This was part of my Laser Physics course under Prof. Adriana Morana and Prof. Emmanuel Marin at [University Jean Monnet](https://www.univ-st-etienne.fr/en/index.html), as part of the [RADMEP](https://master-radmep.org) program. I was with Mario and Luca for these experiments, and in this repository I put the codes I did for data analysis.

## Laboratory 1: Nd:YAG laser system
This experiment explored a simple lser system using Nd:YAG (**N**eodymium-**d**oped **Y**ttrium **A**luminum **G**arnet) as gain medium [[1]](https://en.wikipedia.org/wiki/Nd:YAG_laser). 

Laser, which stands for **L**ight **A**mplification by **S**timulated **E**mission of **R**adiation, generally works through stimulated emission within an optical cavity. An electron absorbs a photon to move into a hgher energy state. However, this current unstable state causes it to go return to its original one, emitting a photon, called spontaneous emission. In the event that another incoming photon conincides with the electron's spontaneous emission, two photons are emitted in what is called _**stimulated emission**_. This **AMPLIFIES** and makes light **COHERENT**.

This is typically achieved with a light source and gain medium to generate emission activities inside an optical cavity of two mirrors on both sides. Each of them are either partially or fully reflected so that there are secondary photons for stimulated emission and aperture for the coherent amplified light to pass. However, there are important factors to consider as well (e.g. temperature, current) to make sure that there is _**population inversion**_, i.e. there are more electrons in the higher states. Otherwise, it is almost impossible to have stimulated emission.

This experiment used a diode laser and Nd:YAG as light source and gain medium, respectively. In the attached Jupyter notebook, `YAG_laser_activity.ipynb`, data analysis was performed to:
- **First**, study the threshold current characteristics of the laser diode. This employs a diode much like an LED, but lasing effect is not achieved without a surplus of electrons in the higher energy states for stimulated emission. The light is not amplified and coherent. Hence, increasing the laser diode's current injects more electrons available for stimulated emission, until the electron's population is sufficient enough to manifest lasing. 





## References
[1] _Nd:YAG laser_, [https://en.wikipedia.org/wiki/Nd:YAG_laser](https://en.wikipedia.org/wiki/Nd:YAG_laser)
