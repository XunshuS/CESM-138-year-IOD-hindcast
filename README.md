# CESM-138-year-IOD-hindcast

This data contains the predicted indices of the Indian Ocean Dipole from the 138-year (1880-2017) retrospective hindcast experiment, by using a ensemble CESM prediction system

## CESM_fc_dmi.nc 
forecasted dmi index   
```
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
```

## initial_jul.nc
initial condition of SSTA and Tsub at 90m for July
```
dimensions:

        time = 138 ;        
        lat  =  65 ;
        lon  = 180 ;
        
variables:
    
        double lon ; # longitude from 0.5 to 358.5 with the resolution of 2deg 
        double lat ; # latitudt from -59.5 to 68.5 with the resolution of 2deg    
        double ssta_jul(time, lat, lon) ; # initial condition of SSTA for July   
        double t90a_jul(time, lat, lon) ; # initial condition of Tsub at 90m for July   
```                
## ssta_fc_04.nc & ssta_fc_07.nc
forecasted SST anomaly from April and July
```
dimensions:
        lon = 144 ;
        lat = 61 ;
        nfc = 6 ;
        ntime = 138 ;
variables:
        double lon(lon) ;
                lon:_FillValue = NaN ;
        int64 lat(lat) ;
        double ssta_fc(nfc, ntime, lat, lon) ;
                ssta_fc:_FillValue = NaN ;
```     
## t90a_fc_04.nc & t90a_fc_07.nc
forecasted subsurface temperature anomaly at 90m (T90a) from April and July
```
dimensions:
        lon = 144 ;
        lat = 61 ;
        nfc = 6 ;
        ntime = 138 ;
variables:
        double lon(lon) ;
                lon:_FillValue = NaN ;
        int64 lat(lat) ;
        double t90a_fc(nfc, ntime, lat, lon) ;
                t90a_fc:_FillValue = NaN ;
``` 
## u850a_fc_04.nc & u850a_fc_07.nc
forecasted zonal wind anomaly at 850hPa from April and July
```
dimensions:
        lon = 144 ;
        lat = 61 ;
        nfc = 6 ;
        ntime = 138 ;
variables:
        double lon(lon) ;
                lon:_FillValue = NaN ;
        int64 lat(lat) ;
        double u850a_fc(nfc, ntime, lat, lon) ;
                u850a_fc:_FillValue = NaN ;
```                      
## v850a_fc_04.nc & v850a_fc_07.nc
forecasted meridional wind anomaly at 850hPa from April and July
```
dimensions:
        lon = 144 ;
        lat = 61 ;
        nfc = 6 ;
        ntime = 138 ;
variables:
        double lon(lon) ;
                lon:_FillValue = NaN ;
        int64 lat(lat) ;
        double v850a_fc(nfc, ntime, lat, lon) ;
                v850a_fc:_FillValue = NaN ;
```                      

## Reference

Song, X., Tang, Y., Liu, T., & Li, X. (2022). Predictability of Indian Ocean Dipole over 138 years using a CESM ensemble-prediction system. Journal of Geophysical Research: Oceans, 127, e2021JC018210. https://doi.org/10.1029/2021JC018210

Song, X., Tang, Y. , Li, X., and Liu, T. (2022). Decadal Variation of Predictability of the Indian Ocean Dipole during 1880–2017 Using an Ensemble Prediction System. Journal of Climate, 35, 5759–5771, https://doi.org/10.1175/JCLI-D-21-0848.1.


If you have any question, please contact songxs@sio.org.cn.
