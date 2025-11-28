# Laser Physics
<p align = "center"><img src = "images/ujm-radmep-logo.png"></p>

This was part of my Laser Physics course under Prof. Adriana Morana and Prof. Emmanuel Marin at [University Jean Monnet](https://www.univ-st-etienne.fr/en/index.html), as part of the [RADMEP](https://master-radmep.org) program. I was with Mario and Luca for these experiments, and in this repository I put the codes I did for data analysis.

## Laboratory 1: Nd:YAG laser system
This experiment explored a simple lser system using Nd:YAG (**N**eodymium-**d**oped **Y**ttrium **A**luminum **G**arnet) as gain medium [[1]](https://en.wikipedia.org/wiki/Nd:YAG_laser). 

Laser, which stands for **L**ight **A**mplification by **S**timulated **E**mission of **R**adiation, generally works through stimulated emission within an optical cavity. An electron absorbs a photon to move into a hgher energy state. However, this current unstable state causes it to go return to its original one, emitting a photon, called spontaneous emission. In the event that another incoming photon conincides with the electron's spontaneous emission, two photons are emitted in what is called _**stimulated emission**_. This **AMPLIFIES** and makes light **COHERENT**.

This is typically achieved with a light source and gain medium to generate emission activities inside an optical cavity of two mirrors on both sides. Each of them are either partially or fully reflected so that there are secondary photons for stimulated emission and aperture for the coherent amplified light to pass. However, there are important factors to consider as well (e.g. temperature, current) to make sure that there is _**population inversion**_, i.e. there are more electrons in the higher states. Otherwise, it is almost impossible to have stimulated emission.

This experiment used a diode laser and Nd:YAG as light source and gain medium, respectively. In the attached Jupyter notebook, `YAG_laser_activity.ipynb`, data analysis was performed to:
- **First**, study the threshold current characteristics of the laser diode at room temperature, 25&deg;C. This employs a diode much like an LED, but lasing effect is not achieved without a surplus of electrons in the higher energy states for stimulated emission. The light is not amplified and coherent. Hence, increasing the laser diode's current injects more electrons available for stimulated emission, until the electron's population is sufficient enough to manifest lasing.
- **Second**, study the absorption characteristics of Nd:YAG at different temperatures.

### Threshold Current
<p align = "center"><img src = "Lab 1 - YAG Laser/1_5_voltage_vs_current.jpg"></p>
<p align = "center"><b>Figure 1.</b> Plot of the diode laser's power, measured as voltage [mV], as function of the injected current. This shows that the minimum threshold to induce lasing happens at 60 mA.</p>

The plot above shows the lasing characteristics of the laser diode used to pump Nd:YAG, depicting the minimum current needed so that population inversion is achieved for stimulated emission.

### Nd:YAG Absoprtion
<p align = "center"><img src = "Lab 1 - YAG Laser/1_5_absorption_vs_temperature_2.jpg"></p>
<p align = "center"><b>Figure 2.</b> Measured absorption characteristics of Nd:YAG with respect to temperature.</p>
The plot above shows that Nd:YAG has higher absorption coefficient at both side of the 20&deg;C-mark. At lower temperatures, absorption decreases up to 20&deg;C and beyon which is increases. This explains the electron population between any two transitional states during photon absorption.

To reiterate the idea, absorption happens when an electron receives a photon, exciting it from a lower to a higher energy state. For a crystal lattice such as Nd:YAG, this absorption happens if there is sufficient electrons in lower states to be excited. The population ratio $P_{i}/P_{0}$ between higher and lower states, respectively, is related to the following proportional expression:

$$\displaystyle \frac{P_{i}}{P_{0}} \propto e^{-\frac{\Delta E}{k_{B}T}}$$

where
- $\Delta E$: Energy difference between these two states
- $k_{B}$: Boltzmann's constant
- $T$: Temperature

Based on this relation, there are more more electrons in the lower state at lower temperatures. This lower state population decreases with increasing temperature, explaining the decline of the absoption coefficient curve below 20&deg;C. However, basing off this relation alone does not explain the increase beyond this temperature mark. As temperature increases, electrons receive sufficient energy to transition into a higher state, depopulating lower state and suppressing more absorption.

It is, however, important to note that as temperature increases, phonons are generated in the crystal lattice which are attributed to the vibrational energy states [[2]](https://en.wikipedia.org/wiki/Phonon). These phonons are the ones who 
assist in this absorption process. _I am not really sure about it but the most plausible explanation I understand is phonon-assisted optical absorption. Although I am not quite sure whether **phonons absorb the photons**, or **photons generate phonons assisting with vibrations in the lattics**. I refer to the information in_ [[3]](https://indico.ictp.it/event/8301/session/99/contribution/546/material/slides/0.pdf) _and_ [[4]](https://www.rp-photonics.com/phonons.html).
## References
[1] _Nd:YAG laser_, [https://en.wikipedia.org/wiki/Nd:YAG_laser](https://en.wikipedia.org/wiki/Nd:YAG_laser).

[2] _Phonon_, [https://en.wikipedia.org/wiki/Phonon](https://en.wikipedia.org/wiki/Phonon).

[3] E. Kioupakis, _Phonon-assisted optical processes_, [https://indico.ictp.it/event/8301/session/99/contribution/546/material/slides/0.pdf](https://indico.ictp.it/event/8301/session/99/contribution/546/material/slides/0.pdf).

[4] R. Paschotta, _Phonons_, [https://www.rp-photonics.com/phonons.html](https://www.rp-photonics.com/phonons.html).
