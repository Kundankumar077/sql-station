# sql-station

SELECT  stars.ID, MONTH(MONTH),round(stars.RAIN_CM *2.54,2) as RAIN_CM,
round((stars.TEMP_F-32)*5/9,2) as TEMP_C, station.CITY,station.STATE,station.LAT_N,station.LONG_W
from stars
inner join station on station.ID= stars.ID;

# ID	CITY	STATE	LAT_N	LONG_W
13	PHONIX	AZ	33	112
44	DANVER	CO	40	105
66	CARBIOU	ME	47	68
# CREATE TABLE `station` (
  `ID` int NOT NULL,
  `CITY` varchar(45) NOT NULL,
  `STATE` varchar(2) NOT NULL,
  `LAT_N` int DEFAULT NULL,
  `LONG_W` int DEFAULT NULL,
  PRIMARY KEY (`ID`)
  # CREATE TABLE `stars` (
  `ID` int NOT NULL,
  `MONTH` date NOT NULL,
  `TEMP_F` float NOT NULL,
  `RAIN_CM` float NOT NULL,
  PRIMARY KEY (`MONTH`)
  # SELECT  stars.ID, MONTH(MONTH),RAIN_CM,TEMP_F, station.CITY,station.STATE
from stars
inner join station on station.ID= stars.ID;
