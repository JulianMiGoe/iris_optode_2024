## iris_optode_2024
Repository to our manuscript "Root-Driven Soil Reduction in Wadden Sea Salt Marshes".

Submitted to Wetlands journal 2024. Accepted Oct 2024

Authors: Julian Mittmann-Goetsch, Monica Wilson, Kai Jensen, Peter Mueller

## Project structure:
      README         
            |data                          # all data frames included in the repository
            |- df_optode_ap                # raw planar optode data of Atriplex portulacoides @Monica Wilson
            |- df_optode_sa                # raw planar optode data of Spartina anglica @Monica Wilson
            |- df_tt_iris                  # IRIS data from the tidal-tank experiment @JulianMiGoe
            |- df_tt_dchange               # IRIS data calculated as delta change values against non-vegetated controls from the tidal-tank experiment @JulianMiGoe
            |- df_tt_ph                    # pH data from the tidal-tank experiment @JulianMiGoe
            |- df_field_iris               # IRIS data from the field study @JulianMiGoe
            |- df_field_dchange            # IRIS data calculated as delta change values against non-vegetated controls from the field study @JulianMiGoe
            |- df_field_ancillary          # ancilliary data from the field study. Calculated as means per plot @JulianMiGoe
            |- df_raw_biomass              # raw biomass data (above- and belowground) from the field study @JulianMiGoe 
            |- df_raw_soil                 # raw soil paramenter data (pH, OM, conductivity) from the field study @JulianMiGoe 
            |- df_DSK_iris                 # IRIS data from Diek-Sander-Koog field study (Mueller et al. 2020) @Peter Mueller 
            |
            |code                          # R code used for the analysis
            |-  iris_optode.RMD            # RMarkdown Skript 

      CODE structure and processing
            | df_optode_ap                 # L0 raw planar optode data of Atriplex portulacoides @Monica Wilson
            |- df_optode_ap_long           # L1 processed data (filtered df_optode_sa to long format table, inlcuding only ROI used for the analysis) - Used to create Figure 4b
            |-- df_optode_ap_long_filtered # L2 processed data from L1 (filtered df_optode_ap_long two slide numbers with drops below 0, slide 40 & slide 159, filtered to only include slides 155-230) - Used to create Figure 4b subpanel
            |
            | df_optode_sa                 # L0 raw planar optode data of Spartina anglica @Monica Wilson
            |- df_optode_sa_long           # L1 processed data (filtered df_optode_ap to long format table, inlcuding only ROI used for the analysis) - Used to create Figure 4a
            |-- df_optode_ap_long_filtered # L2 processed data from L1 (filtered df_optode_sa_long to only include slides 155-230) - USed to create Figure 4a subpanel
            |
            | df_tt_iris                   # L0 IRIS data from the tidal-tank experiment @JulianMiGoe
            |- df_tt_iris_aov              # L1 processed data (filtered df_tt_iris to exclude all NAs) - Used for statistical analysis
            |- df_tt_stat_veg              # L1 processed data (filtered df_tt_iris to exclude all NAs & filtered to only include non-vegetated controls) - Used for statistical analysis
            |- df_tt_a15                   # L1 processed data (filtered df_tt_iris, to include all segments from 0-15cm) - Used to create Figure S1
            |-- df_tt_a15_sum              # L2 processed data (summarised df_tt_a15 to the factor zone)
            |- df_tt_15                    # L1 processed data (filtered df_tt_iris, to only include bottom segment 15-20 cm) 
            |-- df_tt_all_sum              # L2 processed data (summarised df_tt_15 by factor zone) - Used to create Barplot Figure 3a
            |-- df_tt_non_veg              # L2 processed data (filtered df_tt_15 to only include non-vegetated controls) 
            |--- df_tt_non_veg_sum         # L3 processed data (summarised df_tt_non_veg by factor zone) - Used to create Barplot Figure 3b
            |
            |- df_tt_dchange               # L1 processed IRIS data calculated (in Excel) as delta change values against non-vegetated controls from the tidal-tank experiment @JulianMiGoe
            |-- df_tt_dchange_sum          # L2 processed data (summarised df_tt_dchange by factor zone, plant) - Used to create Barplot Figure 3c
            |
            | df_tt_ph                     # L0 raw pH data from the tidal-tank experiment @JulianMiGoe
            |- df_tt_ph_sum                # L1 processed data (summarised df_tt_ph by factor zone, vegetation) - Used to create Figure S2
            |
            | df_field_iris                # L0 raw IRIS data from the field study @JulianMiGoe
            |- df_field_iris_long          # L1 processed data (transformed df_field_iris to long format) 
            |-- df_field_iris_aov          # L2 processed data (filtered df_field_iris_long to exclude all NAs) - Used for statistical analysis
            |-- df_field_elevation         # L2 processed data (summarised df_field_iris_long by factors zone & depth) - Used for Figure S3
            |-- df_field_all               # L2 processed data (summarised df_field_iris_long by factor zone) - Used for Figure 5a
            |-- df_field_subset            # L2 processed data (filtered df_field_iris_long, intermediate dataframe) 
            |--- df_field_unplanted        # L3 processed data (summarised df_field_subset by factor zone, excluded all vegetated plots) - Used for Figure 5b
            |
            | df_field_dchange             # L1 processed IRIS data calculated (in Excel) as delta change values against non-vegetated controls from the field study @JulianMiGoe
            |- df_field_dchange_sum        # L2 processed data (summarised df_field_dchange by factor zone, depth) - Used to create Barplot Figure 5c
            |
            | df_raw_biomass               # L0 raw biomass data (above- and belowground) from the field study @JulianMiGoe 
            | df_raw_soil                  # L0 raw soil paramenter data (pH, OM, conductivity) from the field study @JulianMiGoe 
            |- df_field_ancillary          # L1 processed ancilliary data from the field study. Calculated as means per plot (in Excel from both df_raw_biomass & df_raw_soil) @JulianMiGoe - Used to create Figure 6a-d
            |
            | df_DSK_iris                  # L0 raw IRIS data from Diek-Sander-Koog field study (Mueller et al. 2020) @Peter Mueller 
            | df_DSK_sum                   # L1 processed data (summarised df_DSK_iris by factor zone) - Used to create barplot Figure S5a
            
