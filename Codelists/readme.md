## TSML Codelists
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
- TimeseriesType: all sorts of issues. Entries for DomainRange are duplicated, while TVP is missing. Very strange URI patterns, e.g. [CategoricalTimeseriesDomainRange](http://www.opengis.net/def/timeseriesType/timeseriesML/1.2/Time/CategoricalTimeseriesDomainRange )  `http://www.opengis.net/def/timeseriesType/timeseriesML/1.2/Time/CategoricalTimeseriesDomainRange` 

Unfortunately, there are issues in these lists, some codes are missing, others misspelled (e.g. TotalPrec was listed under PrecTotal). 
Concepts are assigned to many wrong concepts schemes (example on [AvePrec](https://defs.opengis.net/prez/catalogs/ogc-cat:datamodels/col/datamodels:timeseriesml/it1/observationtype:timeseriesML/it2/interpolationcode:AveragePrec))

## Issues with OGC URI Patterns and Updates:

When I look through the various ttl files, I find all sorts of URI Patterns. When I asked Rob, he stated that the URIs should have the pattern:

`http://www.opengis.net/def/{Standard}/{ConceptScheme}/{Concept}`

I've updated all TSML concepts to the correct URI pattern and documented on the TSML GitHub, will provide to Rob for update. 

But, the question is how to deal with all the old ones that went freestyle, some examples I found in TSML:

- http://www.opengis.net/def/observationType/timeseriesML/1.0
- http://www.opengis.net/def/timeseriesType/timeseriesML/
- http://www.opengis.net/def/timeseriesType/timeseriesML/1.2/Time/

### Deprecating

To my view, we should deprecate erroneous URIs, link them to the correct term.

Do I understand correctly that I should add this to my ttl files, provide a sameAs from the new correct URI to the old freestyle one?


### Versioning

Many OGC ConceptSchemes started quite naively, to be defined once, valid for all time. Then reality started biting, updates became necessary, semantics shifting... Some of the TSML URIs I now fixed tried to deal with this, see the "1.0" and "1.2" in some of the URIs, but didn't use an agreed URI pattern.

I'd say the core issue with this is that there isn't an agreed URI pattern to deal with versioning. Should we define one?

Here a suggestion (riffing off the base URI Rob provided):

`http://www.opengis.net/def/{Standard}/{Version}/{ConceptScheme}/{Concept}`

If we had this version addition, we could provide clear concepts per version, as well as provide links between the versions where valid.


## Issues within RAINBOW: 

### Concept resolution

When I resolve a concept, I first get a sort of placeholder page. Here described on the example of http://www.opengis.net/def/timeseries/InterpolationCode/MaxPrec

This first resolves to an alias at https://defs.opengis.net/prez/object?uri=https://www.opengis.net/def/timeseries/InterpolationCode/MaxPrec, tells me the concept is experimental (shouldn't be), a generic definition "This is an alias of the concept referenced by the sameAs predicate."

It does provide a sameAs link, this is more fruitful (difference is the IRI, first is https, 2nd http, what I originally requested), resolves to https://defs.opengis.net/prez/catalogs/ogc-cat:datamodels/col/datamodels:timeseriesml/it1/observationtype:timeseriesML/it2/interpolationcode:MaxPrec, includes the correct definition. Only issue is that the concepts are listed in all TSML concept schemes, not just the correct one.

Is there any way of getting rid of the first page, immediately resolving to the 2nd one as requested?


### Contents of a Concept Scheme

When I go to a concept scheme page, it's still difficult to see members, at least now we have the "members" button at the bottom, once one gets to the right page. Would be nice to have them automatically displayed at the bottom of the page.


### Grouping of all Concepts to ALL Concept Schemes

For some reason, within a standard, all concepts get linked to all Concept Schemes (we also have this issue with the O&M ObservationTypes, I'm seeing a pattern). I've checked the ttl, this cross linking is NOT from the ttl, assuming somehow wrongly entailed. How can we fix this if it wasn't provided, done by behind-the-scenes voodoo?
