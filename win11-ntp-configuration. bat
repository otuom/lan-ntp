REM Change the NTP time server. 
REM Replace FQDN with NTP server domain name or IP adress.
w32tm /config /syncfromflags:manual /manualpeerlist:FQDN

REM Get samples from NTP time server. 
REM Replace FQDN with NTP server domain name or IP adress. 
REM Replace NUMBEROFSAMPLES with number of samples to get.
w32tm /stripchart /computer:FQDN /dataonly /samples:NUMBEROFSAMPLES

REM Uppdate the configuration.
w32tm /config /update

REM Restart Windows Time Service.
net stop w32time
net start w32time

REM Resync system time.
w32tm /resync

REM Open Services settings
services.msc
REM Set "Windows Time" Startup to Automatic
