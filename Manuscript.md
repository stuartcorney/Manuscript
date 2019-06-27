# Title
Performance of Soil Moisture in a Regional Climate Model for Tasmania

<!---
This is how you add a comment
-->

<!---
Tom: Great start Ziliang. I'll have a look through and see how we go. 
-->

Thanks tom I will consider these. Ok. I think we should clean all this up now. 

# Abstract
This project assessed the characteristics of soil moisture across Tasmania in both the Bureau of Meteorology Atmospheric high-resolution Regional Reanalysis (BARRA) and a CSIRO Conformal Cubic Atmospheric model (CCAM) ensemble of simulations. The analysis was over the period 2007-2014 for BARRA and 1961-2100 for CCAM. We compared soil moisture with its related variables (precipitation, temperature and evaporation) to understand the impact of different land surface models within both CCAM and BARRA on their representation of soil moisture. We used BARRA to validate CCAM. We find CCAM and BARRA has similar performance in the surface layers, but different behaviour in the bottom layers. CCAM has high correlation with BARRA in the west region of Tasmania, but not the east region. We explored the seasonal variation of soil moisture in CCAM and how it has been projected to change already, as well as into the future. CCAM has performed well compared to BARRA, the projected future changes across Tasmania are plausible, especially in western Tasmania. Soil moisture is projected to decrease rapidly in this region, with an amplification of trends already observed in the current period in comparison historical conditions.

# Key words
CCAM, BARRA, soil moisture, future change
<!---
These need work. 
-->
I think we need to add some more here

# Acknowledgments
Thank my supervisor team: Dr. Stuart Corney, Dr. Rebecca Harris, Dr. Tom Remenyi and Dr. Peter Love for providing important and very helpful guidance across the honours year. They provide essential information around all aspects used in this project. Thank Dr. Stuart Corney for as the leader of the project. Thank Dr. Tom Remenyi and Dr. Peter Love for the guidance of programming, idea and comments of thesis. Thank Dr. Rebecca Harris for guidance of idea and comments of thesis.

Thank UTAS and OUC for providing the opportunity to do this project in my honours year. Thank Dr. Chun-Hsu Su, Dr. Marcus Thatcher, Dr. Paul Fox-Hughes and Dr. Imtiaz Dharssi for providing essential information about models and soil moisture. 

Thank my family for supporting and encouraging me in my honours year. Thank Roxana Vasile for proofreading my draft. Thank Chengcheng Yang for providing ideas.

Thank staffs in IMAS who provide good research environment. 

# 1. Introduction
With the high intensity of human activities, climate change research has gradually become a hot spot in the field of environment. Many human activities like large-scale burning and extensive land use have increased the concentration of greenhouse gases in the atmosphere, leading to near-surface and atmospheric warming. Global warming affects many aspects of our lives, and has a tremendous impact on the natural environment of the Earth.  

Considering the potential impacts of global warming on soil quality, we have investigated the change in soil moisture in the region of Tasmania. Soil moisture is a measure of how much water is contained in a unit of soil. It plays an important role to both atmosphere and land surface by mediating energy and water fluxes (Peng et al. 2015; Seneviratne et al. 2010).

Soil moisture is affected by many environmental factors, like terrain, precipitation, evaporation and surface land temperature (Kowalczyk et al. 1994). Surface soil moisture can be influenced directly during and following precipitation events, and it can affect the deeper soil moisture indirectly by infiltration. Soil moisture can further affect water availability to plants which can variously control temperature and humidity in the soil (Bramer et al. 2018).

The study of soil moisture has many applications such as agriculture and bushfire control and management. Through the effective simulation of soil moisture, we can learn more information about the condition of vegetation during any period of interest. On one hand, soil moisture content can indirectly indicate how easy it is for the vegetation to extract moisture from the soil (Yamazaki and Miyakawa 2017). On the other hand, the increase in drought and the expansion of dry soil in the climate system can increase the near-surface temperature and reduce evaporation and precipitation, leading to decreased moisture and more frequent bushfires (Harris et al. 2017). 

The variables most closely related to soil moisture are precipitation, surface temperature and evaporation. Since the earliest precipitation records, the global mean precipitation has only been increasing (Hartmann et al. 2013). Global mean surface temperature has rapidly increased since 1880, and the rate at which it increases is faster every decade. In Australia, the change in mean surface temperature follows the global trend. However, the change in evaporation is different among regions (Hartmann et al. 2013). Linked to critical components in the climate system, evaporation can increase with the global mean temperature if the moisture has no limitation, and can increase with soil moisture level.

Precipitation, temperature and evaporation have a direct or indirect relationship with soil moisture. Precipitation will increase soil moisture effectively by adding moisture to the land surface. Temperature has a positive relation with the potential change of evaporation (Seneviratne et al. 2010). Higher temperature can cause high potential increase in evaporation which will directly decrease the moisture content of the soil.

The project’s study area is Tasmania, the island located southeast from mainland Australia. The topography of Tasmania consists of a central plateau, large areas of lowland on the east coastline as well as various mountain ranges in the south, west and north-east regions (Grose et al. 2010; White et al. 2013). In the western part of Tasmania, precipitation is strongly influenced by frontal systems, which are more powerful than the low system, but on the east coast, precipitation is dominated by the low system (Pook et al. 2010; White et al. 2013). Combined with topography and climate, there is a significant precipitation gradient which decreases towards the east. Influenced by the surrounding sea (Grose et al. 2010) and by altitude (White et al. 2013), the lowest temperatures are seen over the central plateau and the highest temperature are seen over the lowland along the east coast. The advantage of looking at Tasmania for assessing the model performance in soil moisture projections lies in its varied topography with precipitation, temperature and evaporation of various magnitudes.

This project proposes the comparison of two methods used for improving model output: downscaling and reanalysis. Both can effectively output more accurate and comprehensive data than the data in global climate models. These two methods have been used in the Conformal Cubic Atmospheric Model (CCAM) and the Bureau of Meteorology atmospheric high-resolution Regional Reanalysis for Australia (BARRA). 

Downscaling means that low-resolution models are converted into more accurate and comprehensive high-resolution models by two optional means. Dynamical downscaling can transfer global climate models (GCMs) into fine-scale regional climate models (RCMs) by a limited area model or a stretched grid global climate model. CCAM uses the stretched grid global climate model method, and BARRA uses the limited area model method. 

Reanalysis uses a collection of observations from different sources for the same area, and then it analyzes the atmospheric data through the data assimilation technique, in order to have a complete, effective evaluation of the model with limited atmospheric observations (Hartmann et al. 2013; Su 2018). At the same time, the reanalysis can estimate unobserved parameters with a limited but irregularly distributed set of observed parameters through some models that have been confirmed to be correct in equation of motion and physical processes (Dee et al. 2014; Su 2018). In order to solve the shortcoming of low-resolution global reanalysis, the dynamical downscaling method was used by embedding high-resolution weather or regional atmospheric models into the low resolution grid of the global reanalysis, making the improved regional reanalysis easier to study in the area of interest (Su 2018).

Regional reanalysis could provide a better assessment of regional climate change through higher temporal and spatial resolution that are more in line with the research requirements (Seneviratne et al. 2010). The first application of reanalysis in Australia is BARRA.

# 2. Materials and methods
## 2.1	Model Description
The Bureau of Meteorology atmospheric high-resolution Regional Reanalysis for Australia (BARRA) is the first reanalysis focused on the region of Australasia, using the one of the European Centre for Medium-Range Weather Forecasts(ECMWF) Reanalysis, ERA-Interim global reanalysis, by embedding the higher resolution and observation-constrained atmospheric Unified Model (UM) (Dee et al. 2011; Su 2018). Data assimilation techniques used in BARRA are implemented in order to correct the dataset using observations from multiple and disparate sources (Dee et al. 2014; Su 2018). The initial production is called BARRA-R, which has approximately 12km lateral resolution throughout Australasia. For local applications and studies, additional high-resolution information is embedded into BARRA-R in order to generate a local-scale regional reanalysis with a 1.5km-horizontal grid resolution (Su 2018). For Tasmania, the BoM generated the BARRA-TA archive (see Table 1). 

The temporal domain of the BARRA-TA simulations is a 10-year period from 2007 to 2016. Over this period BARRA-TA uses two different land-surface models. Between 2007 and 2014 BARRA uses the land component of the UM – the Joint Land Environment Simulator (JULES) (Best et al. 2011). Between 2015 and 2016, BARRA derives its soil moisture from the Bureau's global Numerical Weather Prediction system – the Australian Community Climate and Earth-System Simulator with Global scale (ACCESS-G) (Su 2018), which uses the Met Office Surface Exchange Scheme 2 (MOSES 2) land-surface model to simulate land-surface environment.

JULES can simulate the partitioning of rainfall, atmosphere - biosphere interactions, surface runoff and infiltration (Best et al. 2011) It has four default soil layers of thickness 0.1, 0.25, 0.65 and 2.0 m, giving a total soil depth of 3 m (Table 3) (Best et al. 2011). The soil types are composed of multiple parameters (Figure 1 and Table 2). JULES partitions precipitation into three categories: direct runoff, groundwater recharge and soil moisture storage, and accounts for the fact that groundwater recharge through soil water drainage is slower than direct runoff through surface storage (Best et al. 2011). JULES uses a Probability Distributed Model (PDM) to represent the heterogeneity of soil moisture in sub-grid (Best et al. 2011; Moore, 2007).

ACCESS-G uses the Met Office Surface Exchange Scheme 2 (MOSES 2) as a land-surface model to simulate the land-surface environment. MOSES2 can be used to model climate and predict numerical weather (Essery and Clark 2003). MOSES 2 mostly focuses on the simulation of the land surface variables with heterogeneity in sub-grid, but atmospheric variables and below-the-surface variables like soil moisture are homogeneous in sub-grid. 

The input used in CCAM comes from six global climate models (GCMs) from the Coupled Model Intercomparison Project Phase 5 (CMIP5) (Table 1). Global climate models can provide different estimates of climate change on global scale (Corney et al., 2010). Here, the GCMs are based on the Representative Concentration Pathway (RCP) 8.5 scenarios with very high greenhouse gas emissions (Cubasch et al. 2013).

CCAM has been used extensively in downscaling studies over the past decade or more. (Corney et al. 2010; Engelbrecht et al. 2011; Hoffmann et al. 2016; McGregor 2015; McGregor et al. 2016; Nguyen et al. 2012). It is a variable-resolution global atmospheric model. CCAM uses a conformal-cubic atmospheric model to transfer the six global climate models to the six regional climate models by stretching the grid cells and focusing in the region of Australia through dynamical downscaling (Corney et al. 2010). The six regional climate models by CCAM, referred to as the CCAM-ensemble, have a spatial resolution of 10 km over Tasmania.

Corney et al. (2010) indicates that Regional Climate Models (RCMs) downscaled by CCAM have a high potential to simulate the recent climate change over Tasmania in temperature and precipitation, but with both stochastic and systematic error (Corney et al. 2010). This bias would reflect in the soil moisture differences between CCAM and BARRA-TA, it would increase the uncertainty against observation, and influence the projected trends of soil moisture in the future. 

CCAM-ensemble uses CSIRO Atmosphere Biosphere Land Exchange (CABLE) model to define the plant function types. CABLE can simulate water exchanges between land surface and atmosphere (Kowalczyk et al. 2006), so that it can quantify the soil moisture in regional climate models. In CABLE, soil hydraulic characteristics depend on the moisture content of the soil, frozen or unfrozen, as well as soil type, which are expressed as three parameters (Figure 1 and Table 2) (Kowalczyk et al. 2006).To simulate land-surface environment and soil-vegetation-atmosphere interaction, a canopy scheme (Kowalczyk et al. 1994) is used with six layers (Table 1) for soil moisture, 6 layers for soil temperature, and 3 layers for snow. There is no heat exchange between the moisture and soil because of the vertical movement of water, and soil moisture temperature is the same as the land surface temperature (Kowalczyk et al. 2006). 

Table 1: Description of CCAM-ensemble and BARRA-TA

| Model | Resolution and Domain | Input Models | Period used | Used Variable |
| ----- | --------------------- | ------------ | ----------- | ------------- |
| CCAM     | 10 km, Tasmania       | 6 CMIP5 GCMs: CSIRO-BOM-ACCESS1-0，CNRM-CERFACS-CNRM-CM5，NOAA-GFDL-GFDL-ESM2M，MOHC-HadGEM2-CC，MIROC-MIROC5，NCC-NorESM1-M| Continuous 1961-2019 and 2070-2099  | Soil moisture (m3/m3),Temperature(K), Precipitation (kg/m2/s), Evaporation (kg/m2/s)|
| BARRA-TA | 1.5km, Tasmania       | Content Cell ERA-Interim global reanalysis， United Model (UM)| 2007-2016 | Soil moisture (m3/m3)，Temperature(K)，Precipitation (kg/m2/s)，Evaporation (kg/m2/s)|


![Figure 1](https://github.com/ZiliangTian/Manuscript/blob/master/Figure1.png)

Figure 1: The left is differences in the spatial coverage between CCAM-ensemble and BARRA-TA. Blue is the 10 km-resolution CCAM-ensemble grid and in red indicates the area where the 1.5km0resolution BARRA-TA grid downscaled to 10 km-resolution extends beyond the CCAM-ensemble coverage. The right top one is one of the soil parameters (Volume fraction of condensed water in soil at critical point) in BARRA-TA. The right bottom one is two soil types in CCAM


Table 2: Soil moisture parameters in BARRA-TA and CCAM

| Soil moisture parameters in BARRA-TA | Soil moisture parameters in CCAM |
| ------------------------------------ | -------------------------------- |
| Clapp - Hornberger Coefficient       | Saturation content               | 
| Volume fraction of condensed water in soil at critical point| Wilting content | 
| Snow albedo - free of soil           | Field capacity| 
| Soil bulk density (kg/m3)            |                                  | 
| Saturated soil conductivity after timestep within |                                  | 
| Volume soil moisture content at saturation after timestep within |                                  | 
| Saturated soil water suction         |                                  | 
| Thermal capacity after timestep within |                                  | 
| Thermal conductivity after timestep within |                                  | 

BARRA can provide consistent and accuracy output by the reanalysis methods. Compared with other regional reanalysis in North America, Europe and India, BARRA-TA is more focus on the Tasmania region, with high resolution spatio-temporally (Su 2018). Compared with the regional climate output, BARRA can provide more accuracy data output after bias-correction with the observation. The analysis method calibrates the outputs at hourly interval. It is not identical to the real data even if it is closer to the observation values than other models. For instance in the screen-level temperature, the bias is around zero and is smaller than the control group (ERA-Interim), but some large bias is still present (Jakob et al. 2017). BARRA reanalysis dataset cannot represent the exact real data, but it is more likely to be consistent with the data both spatially and temporally. In this study, we used BARRA-TA reanalysis dataset as a control to assess the CCAM outputs. If the CCAM output dataset is close to BARRA-TA reanalysis dataset, it means that the CCAM outputs are also close to the real scenario in the climate system, or even closer to the real scenario than BARRA-TA reanalysis dataset.

## 2.2	Model Pre-processing
Due to these differences in soil moisture parameterization and different time periods, we must standardise the dataset between CCAM-ensemble and BARRA-TA. 

To facilitate subsequent calculations in grid scale, we first up-scaled BARRA-TA model from the original resolution of 1.5 km to 10 km to match the resolution of CCAM-ensemble. To remap the resolution, we used the second order conservative remapping function within the Climate Data Operator toolkit, which can be applied to any grid on a sphere (Schulzweida et al. 2006). Figure 1 shows the spatial extent of BARRA-TA and CCAM-ensemble with 10 km resolution and the difference between BARRA-TA and CCAM-ensemble. Therefore, in this study, we narrowed the spatial extent of BARRA-TA to match the spatial coverage of CCAM-ensemble. Lastly, values over the sea, which could cause more uncertainty when calculating the statistics over all grid cells, were removed from the analysis.

To allow comparison between BARRA and CCAM, we converted the six soil layers in CCAM into four soil layers matching the soil layers in BARRA (Table 3). Soil moisture is measured in cubic meter per cubic meter (m3/m3), and is considered homogeneous vertically within the same soil layer (Best et al. 2011; Kowalczyk et al. 2006), which can be presented in both CCAM and BARRA-TA. In order to define the new four soil layers in CCAM, we calculated the weighted sum of soil moisture from CCAM’s original six layers relative into the four new layers (Table 3). 

Table 3: Soil layer depth and thickness in CCAM models and BARRA and the weight used to define the four new layers in CCAM to match the ones in BARRA

| Components of BARRA’s Soil Layers | CCAM’s Soil Layers | CCAM’s New Layers |
| --------------------------------- | ------------------ | ----------------- |
| Layer 1: Thickness: 0.100m; Depth range: 0.000 - 0.100m | Layer 1: Thickness: 0.022m; Depth range: 0.000 - 0.022m | Layer 1: 22.0% from CCAM’ s original layer 1; 58.0% from CCAM’ s original layer 2; 20.0% from CCAM’ s original layer 3.|
| Layer 2: Thickness: 0.250m; Depth range: 0.100 - 0.350m | Layer 2: Thickness: 0.058m; Depth range: 0.022 - 0.080m | Layer 2: 53.6% from CCAM’ s original layer 3; 46.4% from CCAM’ s original layer 4.|
| Layer 3: Thickness: 0.650m; Depth range: 0.350 - 1.000m | Layer 3: Thickness: 0.154m; Depth range: 0.080 - 0.234m | Layer 3: 45.1% from CCAM’ s original layer 4; 54.9% from CCAM’ s original layer 5.|
| Layer 4: Thickness: 2.000m; Depth range: 1.000 – 3.000m | Layer 4: Thickness: 0.409m; Depth range: 0.234 - 0.643m | Layer 4: 36.4% from CCAM’ s original layer 5; 63.6% from CCAM’ s original layer 6.|
|                                                         | Layer 5: Thickness: 1.085m; Depth range: 0.643 - 1.728m |                                                                                   |  
|                                                         | Layer 6: Thickness: 2.872m; Depth range: 1.728 - 4.600m |                                                                                   |

## 2.3	Processing
We first explored the relationship between soil moisture and three variables: precipitation, surface temperature and evaporation. Temperature used in this study is the temperature at 1.5 m above land surface. Potential evaporation is referred to as evaporation. Considering the different topography and precipitation in west and east Tasmania, we took one point in each of these regions and compared the monthly time-series over 8 years (2007-2014) between ACCESS-G - one of the CCAM RCMs as an example - and BARRA-TA over soil moisture and related variables. The reason for ACCESS-G is that we found one model’s extreme values were averaged out by the other five models in the ensemble mean. Because of the different unit and magnitude between the variables we considered, for visualizing the change we had to rescale the variation.

Then, we extracted the monthly time-series for soil moisture, precipitation, surface temperature and evaporation for each grid cell from each of RCMs and from BARRA-TA, and we explored the correlation between the range of variables using least squares regression provided by Schulzweida et al. (2006). The correlation values are the mean from individual correlation from each member of the ensemble. We selected the periods 1990-2019 and 2007-2014 in CCAM and in BARRA-TA, respectively.

To compare the soil moisture in CCAM and BARRA-TA, we took the mean of CCAM ensemble. Each grid cell from BARRA-TA and CCAM-ensemble had an eight-year monthly dataset from 2007 to 2014, and a multi-year monthly mean. We used the correlation equation least squares regression provided in Climate Data Operators (Schulzweida et al. 2006) to calculate the mean value between BARRA-TA and CCAM-ensemble. Then we did the statistics of spatial correlation and split the correlation into higher correlation area and low correlation area based on a critical point, which is described in detail below.

In order to calculate the statistics of the spatial correlation, we checked the distribution of correlation values over all grid cells. For this, we chose 21 correlation values between soil moisture and precipitation from 0 to 1 with a 0.05 interval (from -1 to 0 for the negative relationship between soil moisture and other two related variables: temperature and evaporation). We calculated the percentage of grid cells above each correlation value, as well as the average percentage of CCAM-ensemble. Last, we mark the 75% percentage line to better explain the change of curve between models.

For visualizing the spatial distribution within soil moisture between CCAM-ensemble and BARRA-TA, we split each correlation map into two parts: high-confidence areas and low-confidence area based on the critical point.

In choosing the critical point, we decided to:
  * Take the CCAM-ensemble mean. 
  * Consider the first surface soil layer as the standard, because the distribution of the correlation values among the four layers was not consistent. This was justified because the first surface soil layer provides the platform for direct interaction between precipitation, surface temperature, evaporation and soil moisture and it can avoid the contribution of differing hydrological models;
  * Choose the critical correlation point which was the closest to 75% percentage in the first layer in the CCAM-ensemble.

For calculating the seasonal variation, we used the daily soil moisture in layer 1 and 2 for four calendar seasons in 1990-2019 for CCAM-ensemble and 2007-2014 for BARRA-TA. We calculated the seasonal mean at each grid cell for the CCAM-ensemble members.

For the same range of years, we explored the correlation of season variation in layer 1 and layer 2, by calculating the multi-year daily mean values for each season and each grid cell. We calculated correlation values from BARRA-TA and each CCAM-ensemble member by least squares regression, and then calculated the CCAM-ensemble mean. 

We explored the projected values of soil moisture for three time periods: historical (1960-1989), current (1990-2019) and future (2070-2099). We calculated the mean value for each grid cell. We found that RCMs were very similar, therefore we considered the mean of the CCAM-ensemble. We compared the variation of soil moisture in the top two soil layers across 30 years, between historic and current period and between historic and future period. To analyse the seasonal change in soil moisture, we considered four calendar seasons (MAM, SON, DJF, JJA) and compared its variation in the future from historical and current period.

# 3. Results
## 3.1	Internal consistency of soil moisture with other variables
We first investigated the monthly variation of soil moisture with its monthly mean value at two grid cells, one in west Tasmania (Figure 2) and one in east Tasmania (Figure 3) over the common period (2007-2014). The high correlation area in the west means that the west grid cell can be representative for the cells around it and it can be used to explore the relationship between soil moisture and a range of variables. The east grid cell is in a low correlation area and it could show a time-series different from the western area. 

![Figure 2](https://github.com/ZiliangTian/Manuscript/blob/master/Figure2.png)

Figure 2: An example monthly time-series for west Tasmania representing the percentage if change in the monthly mean of soil moisture compared to temperature, precipitation and evaporation for both ACCESS1-0 and BARRA-TA. (Values have been rescaled to a common scale for comparison).

In the west grid cell, the time-series of monthly soil moisture is very similar in all four layers of ACCESS1-0, all showing a strong correlation (or anticorrelation) with precipitation, temperature and evaporation (Figure 2). In BARRA-TA however, there is an obvious lag between the different soil layers, which increases with depth. This lag of more than one month, lead to low correlation of the soil moisture in the bottom layers with surface conditions. Comparing ACCESS1-0 with BARRA-TA, we find that the annual cycle is more obvious in ACCESS1-0 and more intra-annual change is represented in the later. The lag in ACCESS1-0 is small, and is more variable with the lower values of soil moisture. The fluctuation in temperature had less amplitude than other values, which could translate into higher correlation values by least square regression. 

![Figure 3](https://github.com/ZiliangTian/Manuscript/blob/master/Figure3.png)

Figure 3: An example monthly time-series for east Tasmania representing the percentage of change in the monthly mean of soil moisture compared to temperature, precipitation and evaporation for both ACCESS1-0 and BARRA-TA. (Values have been rescaled to a common scale for comparison).

With low evaporation in the east grid cell, the time-series of soil moisture in the top layer 1 fluctuated more than in the other three soil layers (Figure 3). Layers 2 to 4 showed lower values and less correlation in the soil moisture and the three related variables compared to layer 1. Analyzing the precipitation and soil moisture in the four layers, there were more random changes with lower precipitation values than in west region, and the change was dominated by extreme precipitation values each time. In the analysis of each CCAM ensemble member and the CCAM-ensemble mean, we found that one model’s extreme values were averaged out by the other five models. 

Overall, there shows the land surface models have different performance for the soil moisture and its related variables.

We investigated the spatial correlation between soil moisture and three related variables: precipitation, surface temperature and potential evaporation in CCAM-ensemble and compare them with similar metrics from BARRA-TA.

Similar to the correlation of soil moisture between CCAM-ensemble and BARRA-TA, higher correlation values were observed mainly in west Tasmania (Figure 4). Due to the negative relationship between soil moisture and two related variables: surface temperature and potential evaporation – the soil loses moisture with increasing surface temperature and hence increasing potential evaporation – a strong correlation between these variables is indicated by the most negative correlation values (-1). In the spatial distribution, grid cells with high correlations (above 0.5 or below -0.5) were located mostly in western Tasmania, while grid cells with low correlation values (below 0.5 or above -0.5) were located mostly in eastern Tasmania (Figure 4).

In the CCAM-ensemble, the first three layers showed similar pattern of correlation, but lower correlations in bottom layer 4 in all related variables. In BARRA-TA, the lower-correlation grid cells were located predominantly in the eastern Tasmania in the top three layers, and in particular in layer 3. In the fourth layer however, negative-correlation grid cells were distributed all over the study region, with the lowest values predominantly in the east part of Tasmania.

Here is the statistics of the spatial pattern of these correlations. 

For the correlation with precipitation and temperature, CCAM-ensemble had better result of spatial distribution, where the correlation value is higher with 75% percentage than BARRA-TA (Figure 5-A and 5-B). In contrast, BARRA-TA had more grid cells with higher correlation with evaporation of around 75 % than CCAM-ensemble in the first two layers (Figure 5-C).

For the soil layers from surface to bottom, the high correlation (or anticorrelation) area decreased with depth in both CCAM-ensemble and BARRA-TA. There is difference between top layers and bottom layers and also between CCAM-ensemble and BARRA-TA.

![Figure 4](https://github.com/ZiliangTian/Manuscript/blob/master/Figure4.png)

Figure 4: The correlation between soil moisture and a range of variables in CCAM-ensemble from the multi-year monthly mean value over all grid cells in Tasmania, in comparison with BARRA-TA. Here, the resolution of CCAM-ensemble and BARRA-TA is 10km and 1.5km respectively.

![Figure 5](https://github.com/ZiliangTian/Manuscript/blob/master/Figure5.png)

Figure 5: The percentage of grid cells (on y-axis) greater than each correlation value. CCAM-ensemble members are coloured lines, with the CCAM-ensemble mean in black. BARRA-TA is represented as the dark-blue line. The red vertical line marks the 75% of all grid-cells threshold. A-C) shows the correlation between soil moisture and A) precipitation; B) temperature; C) evaporation.

## 3.2	Soil profile and time-series between CCAM and BARRA-TA
First, we investigated the performance of soil layers in CCAM-ensemble compared to BARRA-TA. BARRA-TA and CCAM-ensemble have different soil layers and layer thickness (See Table 3). Figure 6 shows the soil profile in BARRA-TA and CCAM-ensemble after converting the six soil layers in CCAM-ensemble to four new layers that match the soil layers in BARRA-TA.

![Figure 6](https://github.com/ZiliangTian/Manuscript/blob/master/Figure6.png)

Figure 6: Soil profiles of CCAM-ensemble and BARRA-TA in different time periods: a) the six-layers soil profile of CCAM-ensemble from 1990 to 2019; b-d) four-layer soil profile of CCAM-ensemble and BARRA-TA from: b) 1990 to 2019; c) 2007 to 2016; and d) 2007 to 2014. The soil profiles are derived from six (a) or four (in b, c, d) data points at the middle of each soil layer. Soil layer boundaries are represented by the brown long dash line. The data points for each layer is the mean value calculated from models throughout the corrected map range and the whole time period.

The data points for each layer represent the spatial mean value of BARRA-TA and CCAM-ensemble throughout the standardized map range and the whole time period. The profile of the six soil layers in CCAM-ensemble show that the soil moisture increased with depth (Figure 6a). In BARRA-TA, the first three layers were consistent throughout the two time periods (2007-2016 and 2007-2014), with the fourth layer being slightly different between the two periods.

For the CCAM-ensemble, soil moisture increased with depth showing the steepest change between the first and the second layer. In BARRA-TA, soil moisture reached its maximum in the second layer, and then decreased with depth. This suggests that the top two layers of BARRA-TA and CCAM-ensemble have a higher similarity, while the bottom two layers is relatively very different.

![Figure 7](https://github.com/ZiliangTian/Manuscript/blob/master/Figure7.png)

Figure 7: Monthly time-series of soil moisture in BARRA-TA (in black) and CCAM-ensemble (in colour) between 2007-2016. The data is derived from the monthly mean across the entire region of Tasmania.

Figure 7 shows ten years (2007-2016) of monthly time-series of soil moisture in BARRA-TA and CCAM-ensemble. The value is calculated from the mean monthly value across the entire region of Tasmania. In the top two layers, the time-series values were higher in BARRA-TA than in CCAM-ensemble and showed a similar interannual cycle between the two models. In the bottom two layers, the ten-year time-series differed between the two periods (2007-2014 and 2015-2016) of BARRA-TA, with soil moisture values in the first period consistently higher than in CCAM-ensemble. The third soil layer showed a similar interannual cycle in its moisture content, while the fourth layer had a more varied value, with little evidence of an interannual cycle. In the second period of BARRA-TA, the third- and fourth-layer soil moisture values were mostly lower than in CCAM-ensemble. This suggests that these steep changes occur at the transition from JULES to ACCESS-G in BARRA-TA, which are related to the different methods of simulating the land-surface environment between the two time periods. In our evaluation of CCAM-ensemble, we used only the JULES model offline simulation data from 2007 to 2014, with focus on the top two soil layers.

## 3.3	Spatial Correlation of soil moisture between CCAM-ensemble and BARRA-TA
There is the correlation of soil moisture between CCAM-ensemble and BARRA-TA over the entire region of Tasmania. The multi-year monthly mean values showed higher correlation in most grid cells in the first three layers (Figure 8), which could reflect a strong interannual cycle in the CCAM-ensemble. The first two soil layers showed a similar pattern where the correlation values are higher than 0.9 over more than 71% grid cells (Figure 10). The third soil layer was less well correlated, with the lowest correlation in the fourth soil layer, particularly in the southeast corner (where the correlation was also negative) (Figure 10). This correlation decreased towards the east, the lowest value being observed on the east coast of Tasmania. In the fourth layer however, there was a high correlation from inland western Tasmania towards central Tasmania. Very high correlation values were observed in the first three soil layers (Figure 9), with the percentage of grid cells with high correlation rapidly decreasing once below 0.85. In the fourth layer the situation is different. The percentage of grid cells with high correlation decreased consistently.  

![Figure 8](https://github.com/ZiliangTian/Manuscript/blob/master/Figure8.png)

Figure 8: the correlation of monthly annual cycle between soil moisture in CCAM-ensemble and BARRA-TA calculated from the multi-year monthly mean values over all grid cells in Tasmania. Here, the resolution of CCAM-ensemble and BARRA-TA is 10km.

![Figure 9](https://github.com/ZiliangTian/Manuscript/blob/master/Figure9.png)

Figure 9: the percentage of grid cells (y-axis) with correlation values higher than the critical point (x-axis) over all model grid cells for CCAM-ensemble (in colour). The CCAM-ensemble mean value is shown in black for reference.

![Figure 10](https://github.com/ZiliangTian/Manuscript/blob/master/Figure10.png)

Figure 10: Partition of the correlation map by the correlation critical point 0.90. The top (bottom) row shows grid cells with higher (lower) correlation values than the critical correlation point (0.90) from layer 1 to layer 4.

## 3.4	Seasonal Variation
For the seasonal variation, different seasons has different distribution of spatial correlation. In summer, there are more low correlation grid cells in the east region. In Winter, there are more low correlation grid cells in the west and south region, and also the east coastline. The grid cells with high correlation in winter are mostly distributed in the middle and north Tasmania. In autumn and spring, the grid cells with high correlation takes most region but not the east coastline. Overall, the eastern region had a higher number of grid cells with low correlation of seasonal variation in layer 1 and 2 between CCAM-ensemble and BARRA-TA (Figure 11). More extensive areas of low correlation were observed in summer and winter, with the winter low correlation area extending over almost the entire region. 

![Figure 11](https://github.com/ZiliangTian/Manuscript/blob/master/Figure11.png)

Figure 11: The correlation of daily seasonal and annual time-series between soil moisture in CCAM-ensemble and BARRA-TA calculated from the multi-year daily mean values over all grid cells in Tasmania. Here, the resolution of CCAM-ensemble and BARRA-TA is 10km.

## 3.5	Future Change in Seasonal Variation
There has been minimal change between the historical and current periods, where the change is within 5%. In exploration of future projections from the CCAM-ensemble, the general trend indicates that the soil moisture will decrease in the region of Tasmania in the future, with the driest area being projected to be around the central plateau. The east region will get wetter in summer and autumn in the future (Figure 12-B). This wetter area had low correlation of soil moisture between BARRA-TA and CCAM-ensemble (Figure 11). Soil moisture will be lower in all the study region in winter and spring and with less change in the west Tasmania in winter. In regards with the current change (Figure 12-A), the wetter region in the east region is expected to decrease in the future, while the drier region is expected to increase.

![Figure 12](https://github.com/ZiliangTian/Manuscript/blob/master/Figure12.png)

Figure 12: Percentage of change in soil moisture in CCAM-ensemble between three periods: historical (1960-1989), current (1990-2019) and future (2070-2099) and for each season. Columns from one to five correspond to the change in annual, autumn, spring, summer and winter.

# 4. Discussion

## 4.1	The limitation of comparison
Koster et al. (2009) indicate that direct comparison of soil moisture across different models is not accurate due to different model-specific layer thickness or soil texture. In our study, for the comparison of modelled soil moisture, we assimilated the resolution, scale of study, spatial coverage and soil layers. Ultimately, the underlying equations used to derive soil moisture will determine the performance of soil moisture in the model, so we do not attempt to provide an explanation for the differences between the models. Instead, we identify the factors that may be contributing to these differences.

## 4.2	Model difference between BARRA-TA and CCAM  
In 2015/2016, , the base model for regional reanalysis in BARRA was changed from UM to ACCESS-G and the land surface model was changed from JULES to MOSES 2 (Best et al. 2011; Su 2018). The latter model takes different methods to handle the land surface environment (Best et al. 2011; BoM 2010), with more focus on the atmospheric study and increased impact on the absorption of soil moisture around the plant root zone. For the study of soil moisture, we chose to use the JULES operation period in order to provide consistent assessment of CCAM-ensemble, that is, the period 2007-2014.

## 4.3	Soil moisture with related variables from each model
Our results indicate that CCAM-ensemble has higher correlations of soil moisture with precipitation and temperature than BARRA-TA, and higher correlation of soil moisture and evaporation in the first two layers. Best et al. (2011) points to multiple factors influencing surface evaporation, like evapotranspiration and bare soil evaporation. Plant root extraction for evapotranspiration can be another way to transport soil moisture into the atmosphere (Kowalczyk et al. 2006). Similarly, precipitation and surface temperature have a more complicated relationship with soil moisture than linear correlation. Our results could suggest that precipitation and surface temperature have a higher weight in adjusting the soil moisture in CCAM-ensemble than in BARRA-TA, and evaporation has a higher weight to this purpose in BARRA-TA than the CCAM-ensemble. 

Our results showed that the top two layers in both CCAM-ensemble and BARRA-TA have a better representation of the relationship between soil moisture and the variables we investigated than the bottom layers. As shown in Figure 2 and 3, a larger time lag exists in BARRA-TA but only slightly larger in CCAM-ensemble, which could cause lower correlation values in the bottom layers between CCAM-ensemble and BARRA-TA. The correlation values of soil moisture between CCAM-ensemble and BARRA-TA are higher in the west and north Tasmania. In our study we found that the area of high correlation decreases with depth in CCAM-ensemble and BARRA-TA, and much faster in the latter. The different performance through layers, region and between two models could be caused by the different performance of layer, region within soil between CCAM and BARRA-TA, discussed in the following section. 

## 4.4	Difference in soil moisture
## 4.4.1	Soil moisture layer
The mean value in the first two top layers increased with depth for both CCAM-ensemble and BARRA-TA. For the bottom two layers, the soil profile decreased in BARRA-TA but continued to increase in CCAM-ensemble (Figure 6). The time-series of the bottom layers and in particular layer 4, also contained more random interannual variability (Figure 7). Simulation between the top and bottom two layers was different between BARRA-TA and CCAM-ensemble. There is a larger difference between the two surface layers than the bottom two layers.

Previous studies have showed that there are different methods used to model the input and output of layers, handling the drainage of water into the underground water in different ways (Best et al. 2011; Kowalczyk et al. 2006; Moore 2007). JULES and CABLE are more dissimilar in the bottom layers of soil than in the top layers.

When the water from precipitation reaches the ground, whether it infiltrates the top layers of soil or runs off over the surface depends on the tension threshold in soil layers and the outside water capacity (Best et al. 2011). Outside factors such as precipitation, temperature and evaporation, as well as the capacity of surface soil, dominate the partitioning of water and control the infiltration into the surface soil layer for both CCAM-ensemble and BARRA-TA. So, differences between models in top layers are mainly the results of different values, not different methods. The influence of environmental factors (temperature, precipitation and evaporation) are more important than hydrological parameters in the model. 

In the bottom layers, the capacity of soil moisture is dominated by the parameterization of the soil, such as saturation content (See Table 2), to hold moisture and the drainage into the underground water. In CCAM, the CABLE model only uses the field capacity parameter and excess water drains into a groundwater reservoir (and out of the model) (Kowalczyk et al. 2006). In BARRA-TA on the other hand, through JULES, the drainage into groundwater is controlled not only by the field capacity of the soil but also by the absorption capacity of soil, which means that water drainage continues as long as the bottom is oversaturated in moisture (Moore 2007). This difference of an open boundary at the bottom layer explains the more unorderly, random conditions in BARRA-TA. The total depth of original six soil layers is 4.6 m in CCAM and the total depth of four layers is 3.0 m in BARRA-TA. For facilitating the comparison between the two models, we considered the first 3.0 m in CCAM because they are less influenced by the capacity of groundwater and more by the function within the soil layers. This difference could cause a divergence between BARRA-TA and CCAM in the simulations of bottom layers.

Due to different environmental factors and boundary conditions, there is different lag of time between CCAM-ensemble and BARRA-TA and between surface layers and bottom layers. The performance of soil moisture with related variable is more similar in the surface layers than the bottom layers between CCAM-ensemble and BARRA-TA.

## 4.4.2	Soil moisture region
In the spatial correlation of soil moisture between CCAM-ensemble and BARRA-TA, we found the correlation values of soil moisture are higher in the west and north of Tasmania. The topography of south-east Tasmania is mostly lowland, resulting in mostly dry area with lower annual precipitation than the north and west mountainous region (Grose et al. 2010; White et al. 2013). In dry areas, the change of soil moisture is more closely related to episodic precipitation. But in wet areas, soil moisture will dry out or filtrate slowly over time, which can be easier to simulate in both models. Hence in dry areas, the timing of simulated precipitation is crucial for an accurate modelled output of soil moisture.

Technically, the characteristics of soil could be represented by the soil type (Koster et al. 2009). Soil type in BARRA-TA has various change spatially, but is more consistent in the east region than soil type in CCAM (Figure 1). CCAM has only two separate soil types, and has uneven distribution in the east region. Therefore, soil type in BARRA-TA could be more realistic to represent the characteristics of soil. The soil types in BARRA-TA and CCAM are composed of multiple parameters (Table 2), they are constant in time and do not change with precipitation, which can be a limitation, especially for applications on a small spatial scale over a long period of time (Corney et al. 2010).

## 4.4.3	Soil moisture value
We found soil moisture in BARRA-TA was typically higher than in the CCAM-ensemble. Previous studies showed that this could arise from the method used to model the hydrological processes. For example, in JULES, there are two pathways for the water once it reaches the soil surface: infiltration into the soil and surface runoff (Best et al. 2011). In BARRA, JULES has runoff switched off, as the river routing is not included for the limit-area model (Su 2018). In CCAM, CABLE takes surface runoff as one of the dominant factors for the flux of infiltration (Kowalczyk et al. 2006). The large source of water into the soil in BARRA-TA may cause these higher values than CCAM. This study focused on the general trends, rather than the absolute soil moisture values.

## 4.5	Seasonal variation of soil moisture between CCAM-ensemble and BARRA-TA
This study shows a lower correlation between CCAM-ensemble and BARRA-TA over most grid cells in winter compared to the other three seasons. Also, low correlation was observed in the east region in summer, and to a smaller degree in autumn and spring. The grid cells with lower correlation are mostly dry in summer. The difference in seasonal maximums across the four seasons in the CCAM-ensemble and BARRA-TA could cause the lower values observed in the winter.

## 4.6	Future Change in Seasonal Variation
Model predictions show that wetter area could decrease in the future in the east region of Tasmania, while the drier area could increase. This could be caused by the rise of temperature in Tasmania, while the drier area could increase. 

Focusing on the surface layers, which we have more confidence in than the lower layers for the reasons discussed above, shows that the future changes between layer 1 and layer 2 have the same pattern in CCAM-ensemble. Soil moisture in layer 1 has larger change than in layer 2, which could be caused by direct effect with related variables in surface layer 1.

Spatially, the drier area with large magnitude (more than 10% approximately) has higher correlation compared with BARRA-TA than the wetter or slight-changed area in the future. In summer, the correlation between CCAM-ensemble and BARRA-TA shows there are high correlation in the west region in the future change. The west region will become drier than the east region, where the soil moisture will increase or change slightly in the future. In winter, the correlation between CCAM-ensemble and BARRA-TA shows there are lower correlation in the southwest region. In future change, this region is no obvious change or change slightly. 

Supported by BARRA-TA, CCAM can be confident to project the future change in the region, where the soil moisture will decrease rapidly (approximately more than 10 %)

# 5. Conclusion
Our results showed that, in the CCAM-ensemble, soil moisture is better represented in the top two layers than in the bottom layers. In Tasmania, soil moisture has high simulation in the west region and low simulation in the east region, especially the east coastline, where has episodic and drier soil. Compared with BARRA-TA, precipitation and surface temperature in CCAM-ensemble have a higher weight in adjusting soil moisture, but evaporation has low evaporation in adjusting soil moisture in here. In the future, the change would be larger than the current change. The dry region in Tasmania will increase, and the wet region will decrease. Supported by BARRA-TA, CCAM can be confident to project the future change in the region, where the soil moisture will decrease fast (more than 10 % approximately).

# Reference
Best M et al. (2011) The Joint UK Land Environment Simulator (JULES), model description–Part 1: energy and water fluxes Geoscientific Model Development 4:677-699

BoM A (2010) Operational implementation of the ACCESS Numerical Weather Prediction systems NMOC Operations Bulletin 83

Bramer I et al. (2018) Advances in monitoring and modelling climate at ecologically relevant scales. In:  Advances in ecological research, vol 58. Elsevier, pp 101-161

Cubasch U, Wuebbles D, Chen D, et al (2013) Introduction. In ‘Climate Change 2013: The Physical Science Basis. Contribution of Working Group I to the Fifth Assessment Report of the Intergovernmental Panel on Climate Change.’ K Plattner, M Tignor, SK Allen, J Boschung, A Nauels, Y Xia, V Bex, PM Midgley (Cambridge, UK, New York Cambridge Univ Press 2013), http//www Clim org/images/report/WG1AR5_Chapter01_FINAL pdf 119–158. doi: 10.1017/CBO9781107415324.007

Corney S et al. (2010) Climate Futures for Tasmania: climate modelling technical report 

Dee D, Balmaseda M, Balsamo G, Engelen R, Simmons A, Thépaut J-N (2014) Toward a consistent reanalysis of the climate system Bulletin of the American Meteorological Society 95:1235-1248

Dee DP et al. (2011) The ERA‐Interim reanalysis: Configuration and performance of the data assimilation system Quarterly Journal of the royal meteorological society 137:553-597

Engelbrecht FA et al. (2011) Multi-scale climate modelling over Southern Africa using a variable-resolution global model Water Sa 37:647-658 doi:10.4314/wsa.v37i5.2

Essery R, Clark DB (2003) Developments in the MOSES 2 land-surface model for PILPS 2e Global and Planetary Change 38:161-164

Grose M et al. (2010) Climate Futures for Tasmania: general climate impacts technical report 

Harris R, Remenyi T, Fox-Hughes P, Love P, Phillips H, Bindoff N An assessment of the viability of prescribed burning as a management tool under a changing climate: a Tasmanian case study. In: Research Forum 2017: Proceedings from the Research Forum at the Bushfire and Natural Hazards CRC and AFAC Conference, 2017. Bushfire and Natural Hazards CRC, pp 48-63

Hartmann DL et al. (2013) Observations: atmosphere and surface. In:  Climate change 2013 the physical science basis: Working group I contribution to the fifth assessment report of the intergovernmental panel on climate change. Cambridge University Press, 

Hoffmann P, Katzfey JJ, McGregor JL, Thatcher M (2016) Bias and variance correction of sea surface temperatures used for dynamical downscaling Journal of Geophysical Research-Atmospheres 121:12877-12890 doi:10.1002/2016jd025383

Jakob D, Su C, Eizenberg N, Kociuba G, Steinle P, Fox-Hughes P, Bettio L (2017) An atmospheric high-resolution regional reanalysis for Australia Bull Aust Meteorol Oceanogr Soc 30:16-23

Koster RD, Guo Z, Yang R, et al (2009) On the nature of soil moisture in land surface models. J Clim 22:4322–4335. doi: 10.1175/2009JCLI2832.1

Kowalczyk E, Wang Y, Law R, Davies H, McGregor J, Abramowitz G (2006) The CSIRO Atmosphere Biosphere Land Exchange (CABLE) model for use in climate models and as an offline model CSIRO Marine and Atmospheric Research Paper 13:42

Kowalczyk EA, Garratt JR, Krummel PB (1994) Implementation of a soil-canopy scheme into the CSIRO GCM-regional aspects of the model response. CSIRO, 

McGregor JL (2015) Recent developments in variable-resolution global climate modelling Climatic Change 129:369-380 doi:10.1007/s10584-013-0866-5

McGregor JL, Nguyen KC, Kirono DGC, Katzfey JJ (2016) High-resolution climate projections for the islands of Lombok and Sumbawa, Nusa Tenggara Barat Province, Indonesia: Challenges and implications Climate Risk Management 12:32-44 doi:10.1016/j.crm.2015.10.001

Moore R (2007) The PDM rainfall-runoff model Hydrology and Earth System Sciences Discussions 11:483-499

Nguyen KC, Katzfey JJ, McGregor JL (2012) Global 60 km simulations with CCAM: evaluation over the tropics Climate Dynamics 39:637-654 doi:10.1007/s00382-011-1197-8

Peng J, Niesel J, Loew A, Zhang S, Wang J (2015) Evaluation of satellite and reanalysis soil moisture products over southwest China using ground-based measurements Remote sensing 7:15729-15747

Pook M, Risbey J, McIntosh P East coast lows, atmospheric blocking and rainfall: a Tasmanian perspective. In: IOP Conference Series: Earth and Environmental Science, 2010. vol 1. IOP Publishing, p 012011

Schulzweida U, Kornblueh L, Quast R (2006) CDO user’s guide Climate data operators, Version 1

Seneviratne SI et al. (2010) Investigating soil moisture–climate interactions in a changing climate: A review Earth-Science Reviews 99:125-161

Su C-H, Eizenberg, N., Steinle, P., Jakob, D., Fox-Hughes, P., White, C. J., Rennie, S., Franklin, C., Dharssi, I., and Zhu, H. (2018) BARRA v1.0: The Bureau of Meteorology Atmospheric high-resolution Regional Reanalysis for Australia Geoscientific Model Development

White CJ et al. (2013) On regional dynamical downscaling for the assessment and projection of temperature and precipitation extremes across Tasmania, Australia Climate dynamics 41:3145-3165

Yamazaki T, Miyakawa K Soil Moisture Sensing Experiments for Water Management in Pear Fields. In: Proceedings of the 6th International Conference on Informatics, Environment, Energy and Applications, 2017. ACM, pp 56-59

# Appendices
