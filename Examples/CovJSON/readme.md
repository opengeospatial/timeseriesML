## Examples of TSML CovJSON encoding for Domain-Range specialization

### Simple Example (one Observed Property)
#### Example with SOSA Namespace: [Example_Simple_SOSA_NS.jsonld](https://github.com/opengeospatial/timeseriesML/blob/master/Examples/CovJSON/Example_Simple_SOSA_NS.jsonld)
Simple sea surface temperature example, the "temporal" `domain` is enumerated under `values`, t axis contains individual timestamps. The location of the featureOfInterest is included in the `composite` `domain`, `domainType` is defined as PointSeries.

In addition, the `parameters` entry for temperature has been extended with concepts from OMS. The analogous concepts from SOSA are targeted in the context, as SOSA is the semantic realization of OMS. All OMS concepts have a `sosa` prefix.

#### Example without SOSA Namespace: [Example_Simple_SOSA_No_NS.jsonld](https://github.com/opengeospatial/timeseriesML/blob/master/Examples/CovJSON/Example_Simple_SOSA_No_NS.jsonld)
Same example as above, but with SOSA concepts added to the context, thus removing the `sosa` namespace inline

#### Discusion Point: Namespace and Context
The degree of integration with CovJSON is currently under discussion with the CovJSON community, see issues [Additional semantics from OMS](https://github.com/opengeospatial/CoverageJSON/issues/195) and [ssn:observedProperty in context.jsonld and further OMS/SOSA attributes](https://github.com/opengeospatial/CoverageJSON/issues/208)

### Adding Metadata
#### Example with Metadata [Example_Simple_Metadata.json](https://github.com/opengeospatial/timeseriesML/blob/master/Examples/CovJSON/Example_Simple_Metadata.jsonld)
Simple example from above extended with both Point- and TimeseriesMetadata. 

For Point Metadata, the Annotation Coverage approach is utilized. The file [Example_Simple_Annotation.json](https://github.com/opengeospatial/timeseriesML/blob/master/Examples/CovJSON/Example_Simple_Annotation.json) is an Annotation Coverage to this Coverage providing a comment for each value.
#### Discusion Point: Integration with CovJSON
Not yet discussed how to integrate Point- and TimeseriesMetadata within CovJSON. As we're planning on putting Point- and TimeseriesMetadata to an extension of TSML, may make sense to create an independent context for this.


### ToDo
- Multiple ObsProps
- Multiple FoIs

