# Examples of TSML CovJSON encoding

## [Example 1 - Enumerated Domain](https://github.com/opengeospatial/timeseriesML/blob/master/Examples/CovJSON/Example1-EnumeratedDomain.json)
Simple sea surface temperature example, `domain` is enumerated under `values`, t axis contains individual timestamps.

## [Example 2 - Start, End, Num](https://github.com/opengeospatial/timeseriesML/blob/master/Examples/CovJSON/Example2-StartEndNum.json)
Simple sea surface temperature example, `domain` uses `start`, `end` and `num` for t axis.

## [Example 3 - Including spatial information for FoI](https://github.com/opengeospatial/timeseriesML/blob/master/Examples/CovJSON/Example3-FoIStartEndNum.json)
Simple sea surface temperature example, `domain` uses `start`, `end` and `num` for t axis
In addition, the location of the featureOfInterest is included in the `composite` `domain`.

## [Example 4 - OMS](https://github.com/opengeospatial/timeseriesML/blob/master/Examples/CovJSON/Example4-OMSStartEndDomain.json)
Simple sea surface temperature example, `domain` uses `start`, `end` and `num` for t axis
The location of the featureOfInterest is included in the `composite` `domain`
In addition, the `parameters` entry for temperature has been extended with concepts from OMS.



