# WifiProbeSniffer (functional but unfinished)
Wifi probe request sniffer for logging wifi probes near you into a db. 

Small project to tie in with security camera logging to add another layer of information for authorities to investigate in the case of a breakin or incident near your property. 

Bluetooth support is also to be added soon.

Instructions:

# Create mysql database
login to mysql
root@kali: mysql
mysql>
create db
mysql> CREATE DATABASE snifferdb;
create db user
mysql> CREATE USER 'wifiuser'@'localhost' IDENTIFIED BY 'WiFiPa$$word';

mysql> GRANT ALL PRIVILEGES ON snifferdb . * TO 'wifiuser'@'localhost';

mysql> FLUSH PRIVILEGES;

mysql> CREATE TABLE wifi_mac (mac VARCHAR(17), ssid VARCHAR(30), timestamp VARCHAR(20), signal_strength VARCHAR(6))

# Run Script :
you need to put wifi card in monitor mode first
root@kali: airmon-ng start wlan0

root@kali: python wifisniffer1.1.py mon0

