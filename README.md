# contact-tracing
Includes a contact tracing ontology, sample datasets, and sample queries to illustrate the potential of a federated contact tracing system.

To run the sample queries:

1) Set up 2 virtual machines, one with the IP Address 192.168.100.4 and the other with 192.168.100.5
2) Set up Apache Jena Fuseki on both virtual machines: https://jena.apache.org/documentation/fuseki2/
3) Configure Apache Jena Fuseki to use the OWL Mircoreasoner to implement logic: https://jena.apache.org/documentation/inference/index.html
4) Launch Apache Jena Fuseki with the command fuseki-server --update --mem /ds - the server will be located at localhost:3030
5) Upload the desired datasets to the proper machines (192.168.100.4 should have the public health dataset, 192.168.100.5 should have the other datasets)
6) Copy/paste the queries from the ppt. into the engine and run. (Queries 1-4 should be run from 192.168.100.4, query 5 should be run from 192.168.100.5). Be sure to replace <PREFIXES> with the prefixes provided.

Files:
alice5.ttl - public health data
grocery4.ttl - grocery store/employee data
school4.ttl - school data
movie4.ttl - movie theater/social data
blankOntology.owl - the blank Contact Tracing Ontology (with all classes/properties but no individual instances)
Queries - A pdf power point presentation containing 5 sample queries and the results they should return given these datasets. 
  -Query 1 is associated with public health data only
  -Query 2 is associated with public health data and grocery store data
  -Query 3 is associated with public health data and school data
  -Queries 4 & 5 are associated with public health data and movie data
 Query Reasoning - A power point presentation providing information about what each query's situation aware access control is
