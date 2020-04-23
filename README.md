
Cocop.MessageSerialiser.Meas API specification v.2.0
====================================================

---

<img src="logos.png" alt="COCOP and EU" style="display:block;margin-right:auto" />

COCOP - Coordinating Optimisation of Complex Industrial Processes  
https://cocop-spire.eu/

This project has received funding from the European Union's Horizon 2020 research and innovation programme under grant agreement No 723661. This piece of software reflects only the authors' views, and the Commission is not responsible for any use that may be made of the information contained therein.

---


Author
------

Petri Kannisto, Tampere University, Finland  
https://github.com/kannisto  
http://kannisto.org

**Please make sure to read and understand [LICENSE.txt](./LICENSE.txt)!**


COCOP Toolkit
-------------

This application is a part of COCOP Toolkit, which was developed to enable a
decoupled and well-scalable architecture in industrial systems. Please see
https://kannisto.github.io/Cocop-Toolkit/


Introduction
------------

This is a specification for generic APIs that serialise and deserialise (or to
encode and decode) messages that contain measurement values and other data from
industrial systems. Please familiarise yourself with this page:
https://kannisto.github.io/Cocop-Toolkit/messageserialiser.html

The specification consists of XML documents that specify a profile built upon 
standard-based XML schemata. This profile is a subset of what the schemata
specify. These XML documents shall be complied in any implementation of 
Cocop.MessageSerialiser.Meas. Although the XML files do not unambiguously specify
the possible content of the files, they provide guidelines of what features
shall be supported and how they are structured.

The related XML schemata are the following. Each of these standards is
copyrighted to the Open Geospatial Consortium, Inc.(r) For reference and
license information, please see the referred files.

- OGC Filter Encoding 2.0 Encoding Standard – With Corrigendum
  (OGC 09-026r2; please see [ref_and_license_ogc_filter.txt](./ref_and_license_ogc_filter.txt)
- OpenGIS(r) Geography Markup Language (GML) Encoding Standard
  (OGC 07-036; please see [ref_and_license_ogc_gml.txt](./ref_and_license_ogc_gml.txt)
- Observations and Measurements - XML Implementation
  (OGC 10-025r1; please see [ref_and_license_ogc_om.txt](./ref_and_license_ogc_om.txt)
- OGC(r) Sensor Observation Service Interface Standard
  (OGC 12-006; please see [ref_and_license_ogc_sos.txt](./ref_and_license_ogc_sos.txt)
- OGC(r) Sensor Planning Service Implementation Standard
  (OGC 09-000; please see [ref_and_license_ogc_sps.txt](./ref_and_license_ogc_sps.txt)
- OGC(r) SWE Common Data Model Encoding Standard
  (OGC 08-094r1; please see [ref_and_license_ogc_swecommon.txt](./ref_and_license_ogc_swecommon.txt)
- OpenGIS(r) SWE Service Model Implementation Standard
  (OGC 09-001; please see [ref_and_license_ogc_swes.txt](./ref_and_license_ogc_swes.txt)
- TimeseriesML 1.0 – XML Encoding of the Timeseries Profile of Observations and Measurements
  (OGC 15-042r3; please see [ref_and_license_ogc_tsml.txt](./ref_and_license_ogc_tsml.txt)

**Please note**:
* This application has not been certified for compliance with
the abovementioned standards
* This application was not created by the OGC(r)

See also:

* Github repo: https://github.com/kannisto/Cocop.MessageSerialiser.Meas_spec


## XML Files

### "GetObservationRequest.xml" and "GetObservationResponse*.xml"

These files specify message formats for request-response messaging (getting an observation).


### "InsertObservationRequest.xml" and "InsertObservationResponse_*.xml"

These files specify message formats for request-response messaging (inserting an observation).


### "Item_*.xml"

These files specify the data formats for the actual measurement payload. The related metadata has no actual focus.


### "Neg*.xml"

These files are meant to be utilised in the negative testing of applications (i.e., error handling).


### "Observation_*.xml"

These files specify the metadata of observations. The actual measurement values (or other payload) has no actual focus.


### "TaskCancel*.xml"

These files specify messages for task cancellation.


### "TaskGetStatus*.xml"

These files specify messages for querying task status.


### "TaskStatusReport*.xml"

These files specify a message status report.


### "TaskSubmit*.xml"

These files specify messages for starting new tasks.


### "TaskUpdate*.xml"

These files specify messages for updating existing tasks.


### "TemporalFilter_.xml"

These files specify temporal filters (used in GetObservationRequest).


## XSD Files

"cocopcustom*.xsd"

These contain COCOP extensions to the standardised XML schemata. However, please note that the goal is to avoid extensions at all cost.


## Other files

"Data quality.txt"

This file specifies the format of data quality strings.
