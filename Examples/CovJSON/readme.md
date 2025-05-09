# Examples of TSML CovJSON encoding for Domain-Range specialization

## [Example 1 - Enumerated Domain](https://github.com/opengeospatial/timeseriesML/blob/master/Examples/CovJSON/Example1-EnumeratedDomain.json)
Simple sea surface temperature example, the "temporal" `domain` is enumerated under `values`, t axis contains individual timestamps. Note, there is no spatial aspect here yet. This is analogous to PointSeries (see https://docs.ogc.org/cs/21-069r2/21-069r2.html#_8962dcde-77d5-426d-8eeb-ca2c168a0bee) just with no x,y,z designation. 

## [Example 2 - Start, End, Num](https://github.com/opengeospatial/timeseriesML/blob/master/Examples/CovJSON/Example2-StartEndNum.json)
Simple sea surface temperature example, the "temporal" `domain` uses `start`, `end` and `num` for t axis. Note, there is no spatial aspect here yet. This is analogous to PointSeries just with no x,y,z designation.

## [Example 3 - Including spatial information for FoI](https://github.com/opengeospatial/timeseriesML/blob/master/Examples/CovJSON/Example3-FoIStartEndNum.json)
Simple sea surface temperature example, the "temporal" `domain` uses `start`, `end` and `num` for t axis
In addition, the location of the featureOfInterest is included in the `composite` `domain`. This is analogous to PointSeries.

## [Example 4 - OMS](https://github.com/opengeospatial/timeseriesML/blob/master/Examples/CovJSON/Example4-OMSStartEndDomain.json)
Simple sea surface temperature example, `domain` uses `start`, `end` and `num` for t axis
The location of the featureOfInterest (from OMS) is included in the `composite` `domain`
In addition, the `parameters` entry for temperature has been extended with concepts from OMS. This is analogous to PointSeries with additional OMS semantic class extensions.

## [Example 5 - OMS](https://github.com/opengeospatial/timeseriesML/blob/master/Examples/CovJSON/Example5-Metadata.json)
Example 5 extended with both Point and TimeseriesMetadata. `comment-cov.json` is an Annotation Coverage to this Coverage

## ToDo

Multiple ObsProps
Multiple FoIs

