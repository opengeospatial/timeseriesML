Within TSML, we have 5 codelists:
- InterpolationType, more details in the [wiki](https://github.com/opengeospatial/timeseriesML/wiki/Interpolation-Types)
- DataQuality (OK, except for Concepts being in all Schemes)
- ObservationType, use the wrong URI, not cleanly listed in old doc (just in table, no URI)
  - IS: http://www.opengis.net/def/observationType/timeseriesML/1.0/
  - Should be:  http://www.opengis.net/def/timeseries/ObservationType/
- ProcessType (OK, except for Concepts being in all Schemes). Interesting is that here we have narrower terms from WaterML, e.g.
  - http://www.opengis.net/def/timeseries/ProcessTypeCode/Algorithm has the following narrower terms:
    - http://www.opengis.net/def/waterml/2.0/process-type/algorithm
    - http://www.opengis.net/def/waterml/2.0/processType/Algorithm
- TimeseriesType

Unfortunately, there are issues in these lists, some codes are missing, others misspelled (e.g. TotalPrec was listed under PrecTotal). 
Concepts are assigned to many wrong concepts schemes (example on [AvePrec](https://defs.opengis.net/prez/catalogs/ogc-cat:datamodels/col/datamodels:timeseriesml/it1/observationtype:timeseriesML/it2/interpolationcode:AveragePrec))

