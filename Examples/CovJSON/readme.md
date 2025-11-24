# Examples of TSML CovJSON encoding for Domain-Range specialization

## Example with SOSA Namespace: [Example_Simple_SOSA_NS.jsonld](https://github.com/opengeospatial/timeseriesML/blob/master/Examples/CovJSON/Example_Simple_SOSA_NS.jsonld)
Simple sea surface temperature example, the "temporal" `domain` is enumerated under `values`, t axis contains individual timestamps. The location of the featureOfInterest is included in the `composite` `domain`, `domainType` is defined as PointSeries.

In addition, the `parameters` entry for temperature has been extended with concepts from OMS. The analogous concepts from SOSA are targeted in the context, as SOSA is the semantic realization of OMS. All OMS concepts have a `sosa` prefix.

## Example without SOSA Namespace: [Example_Simple_SOSA_No_NS.jsonld](https://github.com/opengeospatial/timeseriesML/blob/master/Examples/CovJSON/Example_Simple_SOSA_No_NS.jsonld)
Same example as above, but with SOSA concepts added to the context, thus removing the `sosa` namespace inline


## [Example 5 - OMS](https://github.com/opengeospatial/timeseriesML/blob/master/Examples/CovJSON/OLD/Example5-Metadata.json)
Example 5 extended with both Point and TimeseriesMetadata. `comment-cov.json` is an Annotation Coverage to this Coverage

## ToDo

Multiple ObsProps
Multiple FoIs

