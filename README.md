# Isgec-Slop-forecasting-module.

This is a Boiler forecasting module where the steam and fuel is getting forecasted. There are 3 parameters to be forecasted.

Main steam per day
Slop per day
Today Bagass
We have data points that we fetch from Kairos db which contains some NA values, 0 values and some exponential values. We need to eliminate it through preprocessing and sometimes if the boiler is off then the values become way too less. So we need to set a criteria that if values are less than or equal to 10 then eliminate. Then Trained the Prophet model to forecast the data for all 3 parameters for 1 month.

Then we push the data back to kairos through kafka.
