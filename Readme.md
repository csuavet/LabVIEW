<a name="user-content-overview" class="anchor" href="#overview" aria-hidden="true"><span class="octicon octicon-link"></span></a>Overview</h1>

<p>This repository contains LabVIEW programs used for controlled-atmosphere thermal demagnetization experiments described in <a href="http://onlinelibrary.wiley.com/doi/10.1002/2013GC005215/full"> Suavet et al. (2014)</a></p>

<h1>
<a name="user-content-contents" class="anchor" href="#contents" aria-hidden="true"><span class="octicon octicon-link"></span></a>Contents</h1>

<h2>
<a name="user-content-controlled_atmosphere" class="anchor" href="#controlled_atmosphere" aria-hidden="true"><span class="octicon octicon-link"></span></a>Controlled_atmosphere</h2>

<p>LabVIEW virtual instrument that calculates the composition of the H<sub>2</sub>-CO<sub>2</sub> gas mixture required to buffer the oxygen fugacity at a given level (in log units relative to the iron-wüstite solid buffer) as a function of temperature. The values are computed using a linear extrapolation to low temperatures of the thermodynamic tables of <a href="http://dx.doi.org/10.1130/0016-7606(1981)92%3C414:COTFTF%3E2.0.CO;2"> Prunier and Hewitt (1981)</a></p><p>
The 'PercentCO2.vi' virtual instrument reads the file 'NewFugTable.csv' that contains the extrapolation data. The file path should be updated before executing the program.</p>

<h2>
<a name="user-content-oven_control" class="anchor" href="#oven_control" aria-hidden="true"><span class="octicon octicon-link"></span></a>Oven_control</h2>

<p>LabVIEW programs that controls the thermal cycle of paleomagnetic oven <a href="http://www.ascscientific.com/td48.htmlASC"> Model TD48-SC</a>:</p><p>
'ASC-FlowControl.vi': main program with user interface.</p><p>
'ASC-OvershootTest.vi': test programs that is used to calibrate the overshoot protection. It sets the temperature at a given value and records the sample temperature. Based on these tests, the values in 'OvershootProtection.vi' sub-VI can be adjusted.</p>
