# Photovoltaik Forecast Module for IP-Symcon
PV Forecast with weather Data from DWD


## Setup
Erstellen einer instanz pvForecast.
Objektparameter pflegen.

Forecast wird stündlich automatisch neu berechnet. (Für den aktuellen Tag bis 10 Uhr, dann wird der Forecast des aktuellen Tages nicht mehr neu berechnet).

## Befehle
Folgende Befehle können in Scripten verwendet werden:

$instance = ID Des PV Forecast Objektes

pvFC_Update (integer $instance, boolean $force);
  $force = true|false :fordert zwingende Aktualisierung an ohne cache
  
pvFC_getForecast(integer $instance): array()
   Liefert die Forecast Daten als Array zurück.

pvFC_getHourForecast(integer $instance, integer $timestamp): integer
   Liefert die vorhergesagten Watt der angegeben Stunde (Timestamp) zurück.

pvFC_getDayForecast(integer $instance, integer $timestamp): integer
   Liefert die vorhergesagten Watt für den angefragten Tag (Timestamp) zurück.


___
(c) 2022 stele99
