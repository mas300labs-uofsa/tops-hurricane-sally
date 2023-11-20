ncks -d time,41112,41351 t2m_2015-2022_hourly.nc t2m_imelda.nc

```
#!/bin/bash
COMMAND="wget"
HPATH="https://www.ncei.noaa.gov/data/north-american-mesoscale-model/access/historical/analysis/201909/"
# Set the value of VARIABLE to an array containing "a", "b", and "c"
YEARMONTH=("201909")
DAY=("10" "11" "12" "13" "14" "15" "16" "17" "18" "19")
HOUR=("0000" "0600" "1200" "1800")
FILE="namanl_218_"
SUFFIX="000.grb2"

for i in "${!DAY[@]}"; do
        for j in "${!HOUR[@]}";do
  echo "$COMMAND $HPATH$YEARMONTH${DAY[i]}/$FILE${YEARMONTH}${DAY[i]}_${HOUR[j]}_${SUFFIX}"
done
done
```

```
#!/bin/bash
COMMAND="wget"
HPATH="https://www.ncei.noaa.gov/data/north-american-mesoscale-model/access/analysis/202009/"
#HPATH="https://www.ncei.noaa.gov/thredds/fileServer/model-namanl/202009/"

# Set the value of VARIABLE to an array containing "a", "b", and "c"
YEARMONTH=("202009")
DAY=("11" "12" "13" "14" "15" "16" "17" "18")
HOUR=("0000" "0600" "1200" "1800")
PRC=("000" "001" "002" "003" "004" "005" "006")
FILE="namanl_218_"
SUFFIX=".grb2"

for i in "${!DAY[@]}"; do
        for j in "${!HOUR[@]}";do
                for k in "${!PRC[@]}";do
  echo "$COMMAND $HPATH$YEARMONTH${DAY[i]}/$FILE${YEARMONTH}${DAY[i]}_${HOUR[j]}_${PRC[k]}${SUFFIX}"
done
done
done
```
