check_em1
=========

checks the em1 sensor box.

### Usage

    check_em1.pl -H host -u sensor_unit -q t|h|w [ -p port ] [ -P web_path ]
    [ -w warn ] [ -c crit ]

Options:

    -H      The ip or hostname of the SnesorTronics EM1 box.
    -p      The port of the webservice running on the EM1, default is 80.
    -P      The webpath for the servicedata, normally '/data'.
    -u      The sensorunit (1-4)
    -q      Which sensor to query (t=temperature, h=humidity, w=wetness)
    -w      The warning threshold.
    -c      The critical threshold.
    -h      Display's this screen here...
    -U      Display's a little usage.

### Threshold Formats

* start <= end

The startvalue have to be less than the endvalue

* start and ':' is not required if start is infinity>

If you set a threshold of '12' it's the same like ':12'

* if range is of format "start:" and end is not specified, assume end is infinity

* alert is raised if metric is outside start and end range (inclusive of endpoints)

* if range starts is lower than end then alert is inside this range (inclusive of endpoints)
