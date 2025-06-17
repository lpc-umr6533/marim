The open-source GATE MARIM database is calculating mean energy deposited per decay in MeV Bq<sup>-1</sup> s<sup>-1</sup> and Dose Conversion Coefficients (DCCs) in μGy h<sup>-1</sup> per Bq kg<sup>-1</sup> produced for 15 𝛼-emitting radionuclides present in 238U and 232Th decay chains for microorganism diameters ranging from 0.5 to 1200 μm.
Fig. 1 summarizes the composition of the database with all parameters (exposures, microorganism diameter, porosity, and radionuclides) considered for this study.

GATE version 9.4 based on Geant4 version 11.2 has been used to calculate energies and DCCs.
Radionuclides were homogeneously distributed in the microorganism (made of liquid water) for internal exposure and in a sphere surrounding the microorganism for external exposure.
When considering external exposure, three different environmental compositions were considered: water, dry sediments (quartz), and a mixture containing 50% of water and 50% of dry sediments.  

A Python Jupyter notebook interface is provided to query the SQL GATE MARIM database and calculate the dose rate received by a microorganism.
As input parameters, the user can select:
- the density (g cm−3) of the medium describing the environment;
- the radionuclide and its activity concentration in the medium (in Bq kg<sup>-1</sup> , or Bq m<sup>−3</sup> , or Bq L<sup>−1</sup>);
- the internal or external exposure;
- the microorganism diameter (between 0.5 μm and 1200 μm).

DCC values were calculated only for 42 different diameters and 3 different porosity values (0%, 50%, and 100%).
For intermediary dimensions, the Python script enables linear interpolations between two consecutive diameters.
For intermediary porosity values, an interpolation using a second-order polynomial fit has been applied.

For more details, have a look at the scientific publication : https://doi.org/10.1016/j.jenvrad.2025.107639.
