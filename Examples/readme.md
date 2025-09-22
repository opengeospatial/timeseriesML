## Encoding Examples for TSML 2.0

Based on community feedback, we're focusing on the following encodings:
- [CovJSON](https://github.com/opengeospatial/timeseriesML/blob/master/Examples/CovJSON/readme.md): Under TSML 1.X, Coverages were provided as the result of an Observation.
This entails quite a bit of redundancy, as Observations and Coverages are stand-alone classes with overlapping attributes.
For TSML 2.0, we're integrating the relevant OMS semantics into the CovJSON Coverage.
- [OGC SensorThings API (STA)](https://github.com/opengeospatial/timeseriesML/blob/master/Examples/STA/readme.md):
STA is natively compliant with the TSML TimeValuePair (TVP) approach.
Only necessary addition is adding TSML Metadata to STA Datastream (TimeseriesMetadata) and Observation (PointMetadata)
- [CSV with W3C CSVW](https://github.com/opengeospatial/timeseriesML/blob/master/Examples/CSV/readme.md):
As many data providers are overwealmed by the provision of APIs, we provide the CSVW approach as a lightweight method of providing timeseries.
Initial work in other projects has demonstrated how this technology can be utilized to automatically transform properly annotated CSV to semantic formats, e.g. SOSA.
