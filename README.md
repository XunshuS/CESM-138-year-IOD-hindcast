# CESM-138-year-IOD-hindcast

This data contains the predicted indices of the Indian Ocean Dipole from the 136-year (1880-2018) retrospective hindcast experiment, by using a ensemble CESM prediction system

  
Source:
        CESM_fc_dmi.nc  # forecasted indices
        
dimensions:
        case = 20 ;        
        lead = 12 ;
        time = 552 ;
        
variables:
        int64 case(case) ;  # number of ensemble members        
        int64 lead(lead) ;  # lead time        
        double time(time) ; # initial time        
                time:_FillValue = NaN ;                
        double dmi(time, case, lead) ; # forecasted DMI index        
                dmi:_FillValue = NaN ;
                
Reference
Song, X., Tang, Y., Liu, T., & Li, X. (2022). Predictability of Indian Ocean Dipole over 138 years using a CESM ensemble-prediction system. Journal of Geophysical Research: Oceans, 127, e2021JC018210. https://doi.org/10.1029/2021JC018210
