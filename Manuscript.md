# Title
Performance of Soil Moisture in a Regional Climate Model for Tasmania

# Abstract
This project assessed the characteristics of soil moisture across Tasmania 
in both the Bureau of Meteorology Atmospheric high-resolution Regional Reanalysis 
(BARRA) and a CSIRO Conformal Cubic Atmospheric model (CCAM) ensemble of 
simulations. The analysis was over the period 2007-2014 for BARRA and 1961-2100 
for CCAM. We compared soil moisture with its related variables (precipitation, 
temperature and evaporation) to understand the impact of different land surface 
models within both CCAM and BARRA on their representation of soil moisture. We 
used BARRA to validate CCAM. We find CCAM and BARRA has similar performance in 
the surface layers than the bottom layers. CCAM has high correlation with BARRA 
in the west region of Tasmania, but not the east region. We explored the seasonal 
variation of soil moisture in CCAM and how it has been projected to change already, 
as well as into the future. CCAM has performed well compared to BARRA, the 
projected future changes across Tasmania are plausible, especially in western 
Tasmania. Soil moisture is projected to decrease rapidly in this region, with an 
amplification of trends already observed in the current period in comparison 
historical conditions.

# Key words
CCAM, BARRA, soil moisture, future change

# Introduction
With the high intensity of human activities, climate change research has gradually 
become a hot spot in the field of environment. Many human activities like large-scale 
burning and extensive land use have increased the concentration of greenhouse gases 
in the atmosphere, leading to near-surface and atmospheric warming. Global warming 
affects many aspects of our lives, and has a tremendous impact on the natural 
environment of the Earth.

Considering the potential impacts of global warming on soil quality, we have 
investigated the change in soil moisture in the region of Tasmania. Soil moisture 
is a measure of how much water is contained in a unit of soil. It plays an important 
role to both atmosphere and land surface by mediating energy and water fluxes 
(Peng et al. 2015; Seneviratne et al. 2010).

Soil moisture is affected by many environmental factors, like terrain, precipitation, 
evaporation and surface land temperature (Kowalczyk et al. 1994). Surface soil moisture 
can be influenced directly during and following precipitation events, and it can affect 
the deeper soil moisture indirectly by infiltration. Soil moisture can further affect 
water availability to plants which can variously control temperature and humidity in 
the soil (Bramer et al. 2018).

The study of soil moisture has many applications such as agriculture and bushfire control 
and management. Through the effective simulation of soil moisture, we can learn more 
information about the condition of vegetation during any period of interest. On one hand, 
soil moisture content can indirectly indicate how easy it is for the vegetation to 
extract moisture from the soil (Yamazaki and Miyakawa 2017). On the other hand, the 
increase in drought and the expansion of dry soil in the climate system can increase 
the near-surface temperature and reduce evaporation and precipitation, leading to 
decreased moisture and more frequent bushfires (Harris et al. 2017). 

The variables most closely related to soil moisture are precipitation, surface temperature 
and evaporation. Since the earliest precipitation records, the global mean precipitation 
has only been increasing (Hartmann et al. 2013). Global mean surface temperature has 
rapidly increased since 1880, and the rate at which it increases is faster every decade. 
In Australia, the change in mean surface temperature follows the global trend. However, 
the change in evaporation is different among regions (Hartmann et al. 2013). Linked to 
critical components in the climate system, evaporation can increase with the global mean 
temperature if the moisture has no limitation, and can increase with soil moisture level.

Precipitation, temperature and evaporation have a direct or indirect relationship with soil 
moisture. Precipitation will increase soil moisture effectively by adding moisture to the 
land surface. Temperature has a positive relation with the potential change of evaporation 
(Seneviratne et al. 2010). Higher temperature can cause high potential increase in evaporation 
which will directly decrease the moisture content of the soil.

The project’s study area is Tasmania, the island located southeast from mainland Australia. 
The topography of Tasmania consists of a central plateau, large areas of lowland on the east 
coastline as well as various mountain ranges in the south, west and north-east regions 
(Grose et al. 2010; White et al. 2013). In the western part of Tasmania, precipitation is 
strongly influenced by frontal systems, which are more powerful than the low system, but on 
the east coast, precipitation is dominated by the low system (Pook et al. 2010; White et al. 2013). 
Combined with topography and climate, there is a significant precipitation gradient which 
decreases towards the east. Influenced by the surrounding sea (Grose et al. 2010) and by 
altitude (White et al. 2013), the lowest temperatures are seen over the central plateau and 
the highest temperature are seen over the lowland along the east coast. The advantage of 
looking at Tasmania for assessing the model performance in soil moisture projections lies 
in its varied topography with precipitation, temperature and evaporation of various magnitudes.

This project proposes the comparison of two methods used for improving model output: downscaling
and reanalysis. Both can effectively output more accurate and comprehensive data than the data in 
global climate models. These two methods have been used in the Conformal Cubic Atmospheric Model 
(CCAM) and the Bureau of Meteorology atmospheric high-resolution Regional Reanalysis for Australia 
(BARRA). 

Downscaling means that low-resolution models are converted into more accurate and comprehensive 
high-resolution models by two optional means. Dynamical downscaling can transfer global climate 
models (GCMs) into fine-scale regional climate models (RCMs) by a limited area model or a stretched 
grid global climate model. CCAM uses the stretched grid global climate model method, and BARRA uses 
the limited area model method. 

Reanalysis uses a collection of observations from different sources for the same area, and then it 
analyzes the atmospheric data through the data assimilation technique, in order to have a complete, 
effective evaluation of the model with limited atmospheric observations (Hartmann et al. 2013; 
Su 2018). At the same time, the reanalysis can estimate unobserved parameters with a limited but 
irregularly distributed set of observed parameters through some models that have been confirmed to
be correct in equation of motion and physical processes (Dee et al. 2014; Su 2018). In order to 
solve the shortcoming of low-resolution global reanalysis, the dynamical downscaling method was 
used by embedding high-resolution weather or regional atmospheric models into the low resolution 
grid of the global reanalysis, making the improved regional reanalysis easier to study in the area 
of interest (Su 2018).

Regional reanalysis could provide a better assessment of regional climate change through higher 
temporal and spatial resolution that are more in line with the research requirements (Seneviratne 
et al. 2010). The first application of reanalysis in Australia is BARRA.
 
# Materials and methods
## 2.2.1	Model Description
The Bureau of Meteorology atmospheric high-resolution Regional Reanalysis for Australia (BARRA) is the first reanalysis focused on the region of Australasia, using the one of the European Centre for Medium-Range Weather Forecasts(ECMWF) Reanalysis, ERA-Interim global reanalysis, by embedding the higher resolution and observation-constrained atmospheric Unified Model (UM) (Dee et al. 2011; Su 2018). Data assimilation techniques used in BARRA are implemented in order to correct the dataset using observations from multiple and disparate sources (Dee et al. 2014; Su 2018). The initial production is called BARRA-R, which has approximately 12km lateral resolution throughout Australasia. For local applications and studies, additional high-resolution information is embedded into BARRA-R in order to generate a local-scale regional reanalysis with a 1.5km-horizontal grid resolution (Su 2018). For Tasmania, the BoM generated the BARRA-TA archive (see Table 1). 

The temporal domain of the BARRA-TA simulations is a 10-year period from 2007 to 2016. Over this period BARRA-TA uses two different land-surface models. Between 2007 and 2014 BARRA uses the land component of the UM – the Joint Land Environment Simulator (JULES) (Best et al. 2011). Between 2015 and 2016, BARRA derives its soil moisture from the Bureau's global Numerical Weather Prediction system – the Australian Community Climate and Earth-System Simulator with Global scale (ACCESS-G) (Su 2018), which uses the Met Office Surface Exchange Scheme 2 (MOSES 2) land-surface model to simulate land-surface environment.

JULES can simulate the partitioning of rainfall, atmosphere - biosphere interactions, surface runoff and infiltration (Best et al. 2011) It has four default soil layers of thickness 0.1, 0.25, 0.65 and 2.0 m, giving a total soil depth of 3 m (Table 3) (Best et al. 2011). The soil types are composed of multiple parameters (Figure 1 and Table 2). JULES partitions precipitation into three categories: direct runoff, groundwater recharge and soil moisture storage, and accounts for the fact that groundwater recharge through soil water drainage is slower than direct runoff through surface storage (Best et al. 2011). JULES uses a Probability Distributed Model (PDM) to represent the heterogeneity of soil moisture in sub-grid (Best et al. 2011; Moore, 2007).

ACCESS-G uses the Met Office Surface Exchange Scheme 2 (MOSES 2) as a land-surface model to simulate the land-surface environment. MOSES2 can be used to model climate and predict numerical weather (Essery and Clark 2003). MOSES 2 mostly focuses on the simulation of the land surface variables with heterogeneity in sub-grid, but atmospheric variables and below-the-surface variables like soil moisture are homogeneous in sub-grid. 

The input used in CCAM comes from six global climate models (GCMs) from the Coupled Model Intercomparison Project Phase 5 (CMIP5) (Table 1). Global climate models can provide different estimates of climate change on global scale (Corney et al., 2010). Here, the GCMs are based on the Representative Concentration Pathway (RCP) 8.5 scenarios with very high greenhouse gas emissions (Cubasch et al. 2013).

CCAM has been used extensively in downscaling studies over the past decade or more. (Corney et al. 2010; Engelbrecht et al. 2011; Hoffmann et al. 2016; McGregor 2015; McGregor et al. 2016; Nguyen et al. 2012). It is a variable-resolution global atmospheric model. CCAM uses a conformal-cubic atmospheric model to transfer the six global climate models to the six regional climate models by stretching the grid cells and focusing in the region of Australia through dynamical downscaling (Corney et al. 2010). The six regional climate models by CCAM, referred to as the CCAM-ensemble, have a spatial resolution of 10 km over Tasmania.

Corney et al. (2010) indicates that Regional Climate Models (RCMs) downscaled by CCAM have a high potential to simulate the recent climate change over Tasmania in temperature and precipitation, but with both stochastic and systematic error (Corney et al. 2010). This bias would reflect in the soil moisture differences between CCAM and BARRA-TA, it would increase the uncertainty against observation, and influence the projected trends of soil moisture in the future. 

CCAM-ensemble uses CSIRO Atmosphere Biosphere Land Exchange (CABLE) model to define the plant function types. CABLE can simulate water exchanges between land surface and atmosphere (Kowalczyk et al. 2006), so that it can quantify the soil moisture in regional climate models. In CABLE, soil hydraulic characteristics depend on the moisture content of the soil, frozen or unfrozen, as well as soil type, which are expressed as three parameters (Figure 1 and Table 2) (Kowalczyk et al. 2006).To simulate land-surface environment and soil-vegetation-atmosphere interaction, a canopy scheme (Kowalczyk et al. 1994) is used with six layers (Table 1) for soil moisture, 6 layers for soil temperature, and 3 layers for snow. There is no heat exchange between the moisture and soil because of the vertical movement of water, and soil moisture temperature is the same as the land surface temperature (Kowalczyk et al. 2006). 




# Results

# Discussion

# Conclusion

# Acknowledge

# Appendices
