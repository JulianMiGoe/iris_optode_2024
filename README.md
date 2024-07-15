# iris_optode_2024
Repository to our manuscript "Root-Driven Soil Reduction in Wadden Sea Salt Marshes".

Submitted to Wetlands journal 2024. 

Authors: Julian Mittmann-Goetsch, Monica Wilson, Kai Jensen, Peter Mueller

Project structure:
README         
data                     # all raw and processed data
|- df_atriplex_optode     # raw planar optode data of Atriplex portulacoides @Monica Wilson
|- df_spartina_optode     # raw planar optode data of Spartina anglica @Monica Wilson
|- df_tt_iris             # IRIS data from the tidal-tank experiment @JulianMiGoe
|- df_tt_dchange          # IRIS data calculated as delta change values against non-vegetated controls from the tidal-tank experiment @JulianMiGoe
|- df_tt_ph               # pH data from the tidal-tank experiment @JulianMiGoe
|- df_field_iris          # IRIS data from the field study @JulianMiGoe
|- df_field_dchange       # IRIS data calculated as delta change values against non-vegetated controls from the field study @JulianMiGoe
|- df_field_ancillary     # ancilliary data from the field study. Calculated as means per plot @JulianMiGoe
|- df_raw_biomass         # raw biomass data (above- and belowground) from the field study @JulianMiGoe 
|- df_raw_soil            # raw soil paramenter data (pH, OM, conductivity) from the field study @JulianMiGoe 
|- df_DSK_iris            # IRIS data from Diek-Sander-Koog field study (Mueller et al. 2020) @Peter Mueller 
            
code                     # R code used for the analysis
|-  iris_optode.RMD       # reference files to be used in analysis

