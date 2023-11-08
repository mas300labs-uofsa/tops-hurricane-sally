https://www.ncei.noaa.gov/has/HAS.FileAppRouter?datasetname=NAMANL218&subqueryby=STATION&applname=&outdest=FILE

September 17-19, 2019


September 10
- https://en.wikipedia.org/wiki/Tropical_Storm_Imelda


Expanse
```
cd $SCRATCH
cd imelda
./script_imelda.sh > getimelda.sh
chmod u+x getimelda.sh
./getimelda.sh
```

It is 1.9GB
```
(base) [llowe@login01 imelda]$ du -d 0 -h .
1.9G	.
```

Make python environment
```
conda create --prefix ~/env_nam cfgrib
```




